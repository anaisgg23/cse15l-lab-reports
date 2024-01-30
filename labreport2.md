# LAB REPORT #2 Servers and SSH Keys
---
## Part 1
`ChatServer` code:
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    String list = "";
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return "";
        } else {
            if (url.getPath().contains("/add")) {
                int i = url.getQuery().indexOf("&");
                String message = url.getQuery().substring(2,i);
                String[] users = url.getQuery().split("user=");
                list += (String.format("%s: %s\n", users[1], message));
                return String.format(list);
            }
            return "404 Not Found!";
        }
    }
}

class ChatServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/df6df832-0e94-4a49-a02f-827308ecaff5)
* The methods being called in my code is the handleRequest method. The `main` method and `Server.start` method are called being this screenshot, when the server is being created. 
* What are the relevant arguments to those methods, and the values of any relevant fields of the class
* How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.

![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/9c6d2f0c-b267-4844-bcf8-42d677ad0678)
* The method being called is the `handleRequest` method. 
* What are the relevant arguments to those methods, and the values of any relevant fields of the class
* How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
---
## Part 2
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/4bdb1a0d-f21b-4265-ae06-5b3bbbd98099)
* The absolute path to the private key for my SSH key for logging into ieng6 is the one highlighted in pink.
* The absolute path to the public key for my SSH key for logging into ieng6 is the one highlighted in yellow.

A terminal interaction where I log into my ieng6 account without being asked for a password:
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/07def0ea-ef1e-44f4-ad4e-db8aef4d0a6c)

---
## Part 3
