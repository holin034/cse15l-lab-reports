# Lab Report 2
## Creating a Web Server
- Code of my StringServer: 
```
import java.io.IOException;
import java.net.URI;
import java.util.*;

class Handler implements URLHandler {
    ArrayList<String> list = new ArrayList<>();

    public String handleRequest(URI url) {
        String str = "";
        String printOut = "";
        if (url.getPath().equals("/")) {
            return str;
        }
        else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    list.add(parameters[1]);
                    for (int i = 0; i < list.size(); i++) {
                        printOut += list.get(i) + "\n";
                    }
                    return printOut;
                }
            }
            return "404 Not Found!";
        }
    }
}

class StringServer {
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

