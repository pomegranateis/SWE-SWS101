# Evidences 

### XSS

If the victim user has privileged access within the application, then the attacker might be able to gain full control over all of the application's functionality and data.

![alt text](<Screenshot from 2024-05-29 10-47-58.png>)

The above is an example of injecting a harmful html code. It can be more affectful if javascript could also be used.

![alt text](<Screenshot from 2024-05-30 18-11-46.png>)
![alt text](<Screenshot from 2024-05-30 18-15-40.png>)

Something like these.

![alt text](<Screenshot from 2024-05-31 11-03-29.png>)

Once the upload is completed, we are provided with an https link to access our file directly from the browser

![alt text](<Screenshot from 2024-05-31 11-02-49.png>)

In developer mode, we can confirm the cookie value

![alt text](<Screenshot from 2024-05-31 11-03-07.png>)

The cookie content is consistent with the server side code

![alt text](<Screenshot from 2024-05-29 18-48-17.png>)

This is how it will apply.

### Privilege escalation

If a user can gain access to functionality that they are not permitted to access then this is vertical privilege escalation. For example, if a non-administrative user can gain access to an admin page where they can delete user accounts, then this is vertical privilege escalation.

![alt text](<Screenshot from 2024-05-30 18-55-56.png>)

The above is an example of URL parameter manipulation attempting to update a profile with an is_admin parameter set to **True**, which could grant the user administrative privileges if the application does not properly validate or sanitize this input.

Its an attack vector where an attacker manipulates URL parameters to gain unauthorized access or escalate privileges within a web application. 

![alt text](<Screenshot from 2024-05-29 18-51-32.png>)

If i log back in again, I will be displayed as the admin and the author of the website with all granted privileges to manipulate any data in it.

![alt text](<Screenshot from 2024-05-29 18-22-26.png>)

### Cookie manipulation

An attacker may be able to use this vulnerability to construct a URL that, if visited by another user, will set an arbitrary value in the user's cookie.

![alt text](<Screenshot from 2024-05-30 19-58-36.png>)

This exploits a vulnerability by passing multiple user identifiers (uid) separated by a pipe character (|). This pattern suggests an attempt to bypass user authorization checks by specifying multiple user roles in a single parameter. If the application does not properly parse and validate the uid parameter, treating it as a single value rather than a list or array, it could lead to privilege escalation or unauthorized access.

![alt text](<Screenshot from 2024-05-30 20-20-39.png>)
![alt text](<Screenshot from 2024-05-29 19-17-20.png>)

### Path Traversal

This enable an attacker to read arbitrary files on the server that is running an application.

Attacker can write to arbitrary files on the server, allowing them to modify application data or behavior, and ultimately take full control of the server.

For instance, **%2e%2e%2f** represents **../** in URL-encoded form.

![alt text](<Screenshot from 2024-05-29 19-20-53.png>)

Here, **..%/2fsecret.txt** attempts to navigate up one directory from the current location and then access a file named secret.txt.

This exposes hidden data out to plain sight.

