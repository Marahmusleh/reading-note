# The HTTP Request Lifecycle

### Step 1: Local Processing

The browser will then look through its own cache of recently requested URLs, the operating system’s cache of recent queries, your router’s cache, and your DNS cache.

### Step 2 : Resolve an IP

Like the processing done locally, resolving an IP from a "DNS server" is a sequence that includes many steps, and includes failovers if the first request fails to return an address.
### Step 3: Establish a TCP connection

 Now that the client has an IP address, it can send an HTTP request, right? Almost, but first, since the request is sent over TCP, which is a transport layer protocol like UDP, the client must open a TCP connection.
 
### Step 4: Send HTTP Request

 Now that the client has an IP address and a TCP connection, it can finally send an HTTP request.
 
 ### Step 5: Tearing Down and Cleaning Up

 Tearing Down and Cleaning Up Four way handshake signals will be made between the client and the server to end the TCP connection between them.

 # Java HTTP Request example
1. HttpUrlConnection
The HttpUrlConnection class allows us to perform basic HTTP requests without the use of any additional libraries. All the classes that we need are part of the java.net package.
2. Creating a Request
We can create an HttpUrlConnection instance using the openConnection() method of the URL class. Note that this method only creates a connection object but doesn't establish the connection yet.
>URL url = new URL("http://example.com"); 
HttpURLConnection con = (HttpURLConnection) url.openConnection(); 
con.setRequestMethod("GET");

3. Adding Request Parameters
If we want to add parameters to a request, we have to set the doOutput property to true, then write a String of the form param1=value¶m2=value to the OutputStream of the HttpUrlConnection instance.
4. Setting Request Headers

Adding headers to a request can be achieved by using the setRequestProperty() method:
>con.setRequestProperty("Content-Type", "application/json");

5. Configuring Timeouts
HttpUrlConnection class allows setting the connect and read timeouts. These values define the interval of time to wait for the connection to the server to be established or data to be available for reading.

To set the timeout values, we can use the setConnectTimeout() and setReadTimeout() methods:

>con.setConnectTimeout(5000); con.setReadTimeout(5000);

6. Handling Cookies
The java.net package contains classes that ease working with cookies such as CookieManager and HttpCookie.
7. Handling Redirects
We can enable or disable automatically following redirects for a specific connection by using the setInstanceFollowRedirects() method with true or false parameter:
>con.setInstanceFollowRedirects(false);

8. Reading the Response
Reading the response of the request can be done by parsing the InputStream of the HttpUrlConnection instance.

To execute the request, we can use the getResponseCode(), connect(), getInputStream() or getOutputStream() methods:

>int status = con.getResponseCode();

9. Reading the Response on Failed Requests
If the request fails, trying to read the InputStream of the HttpUrlConnection instance won't work. Instead, we can consume the stream provided by HttpUrlConnection.getErrorStream().
10 .Building the Full Response It's not possible to get the full response representation using the HttpUrlConnection instance.

