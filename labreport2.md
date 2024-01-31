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
* The methods being called in my code is the `handleRequest` method. The `main` method and `Server.start` method are called being this screenshot, when the server is being created. 
* The relevant arguments are the values "Hi!" and "Anais". The values of any relevant fields are `int i = 4`, `String message = "Hi"` and `String[] users = "Anais"`
* The values of i, message, users, and list change as i is set to the index of "&" in the argument, message is changed to the substring between index 2(which is after "s=") and index i, user is changed to whatever is after "user=" in the argument, and list is changed as the new formatted string in added.

![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/9c6d2f0c-b267-4844-bcf8-42d677ad0678)
* The method being called is the `handleRequest` method. 
* The relevant arguments are the values "Hey!" and "Anais". The values of any relevant fields are `int i = 6`, `String message = "Hey"` and `String[] users = "Anais"`
* The values of i, message, users, and list change as i is set to the index of "&" in the argument, message is changed to the substring between index 2(which is after "s=") and index i, user is changed to whatever is after "user=" in the argument, and a new formatted stirng is added to list which as this point already has the past formatted strings.

---
## Part 2
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/c4c1b0f1-d32a-41ab-9879-9401c0b1cb93)
* The absolute path to the private key for my SSH key for logging into ieng6 is `id_ed25519`.
* The absolute path to the public key for my SSH key for logging into ieng6 is `id_ed25519.pub`.

**A terminal interaction where I log into my ieng6 account without being asked for a password:**
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/07def0ea-ef1e-44f4-ad4e-db8aef4d0a6c)

---
## Part 3
* Everything that was covered in lab 2 and 3 from making servers to using SSH keys I did not know anything about before. I learned how to create ports and servers and was able to learn from past examples how the code for setting up methods for these servers work. In addition I learned so much about SSH keys from how to create them to how to create on where I do not need to input my password. 
