# LAB REPORT #2 Servers and SSH Keys
---
## Part 1
ChatServer code:
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
---
## Part 2
---
## Part 3
