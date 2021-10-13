# Hashing Passwords: One-Way Road to Security

### Storing Passwords is Risky and Complex
A simple approach to storing passwords is to create a table in our database that maps a username with a password. When a user logs in, the server gets a request for authentication with a payload that contains a username and a password. We look up the username in the table and compare the password provided with the password stored. A match gives the user access to the application.

The security strength and resilience of this model depends on how the password is stored. The most basic, but also the least secure, password storage format is cleartext.

### What's Hashing About?
 hashing refers to "chopping something into small pieces" to make it look like a "confused mess". That definition closely applies to what hashing represents in computing.

 ![img](https://images.ctfassets.net/23aumh6u8s0i/ES2U6Gx7w0yVF9Asidr26/75531c3695f09272142b543a94acc0de/hash-flow)

* The core purpose of hashing is to create a fingerprint of data to assess data integrity.
* A hashing function takes arbitrary inputs and transforms them into outputs of a fixed length.
* To qualify as a cryptographic hash function, a hash function must be pre-image resistant and collision resistant.
* Due to rainbow tables, hashing alone is not sufficient to protect passwords for mass exploitation. To mitigate this attack vector, hashing must integrate the use of cryptographic salts.
* Password hashing is used to verify the integrity of your password, sent during login, against the stored hash so that your actual password never has to be stored.
* Not all cryptographic algorithms are suitable for the modern industry. At the time of this writing, MD5 and SHA-1 have been reported by Google as being vulnerable due to collisions. The SHA-2 family stands as a better option.

## The BCrypt Solution

Using a Key Factor, BCrypt is able to adjust the cost of hashing. With Key Factor changes, the hash output can be influenced. In this way, BCrypt remains extremely resistant to hacks, especially a type of password cracking called rainbow table.

This Key Factor will continue to be a key feature as computers become more powerful in the future. because it compensates for these powerful computers and slows down hashing speed significantly. Ultimately slowing down the cracking process until it’s no longer a viable strategy.

If you have sensitive data or information that you need to be protected, ensuring it is secured correctly is vital. As we have seen, there are many ways to secure this information through various password methods, but only BCrypt offers a truly robust solution.

