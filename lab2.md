# Lab Report 2
Note: I have adapted this tutorial to Mac users only as I only have access to a Macbook.
## Writing StringServer
* Below is the code for the StringServer.java file that I used to create the StringServer web server:
`import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    String toShow = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return toShow;
        } 
        else {
            if (url.getPath().contains("/add-message")) {
                String[] queryParam = url.getQuery().split("=");
                if (queryParam[0].equals("s")) {
                    toShow = String.format("\n"+"%s",queryParam[1]);
                    return toShow;
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
`

* After downloading, run the installer. 
* Once it has been installed, run the program and it should open up a window that looks like this (Ignore the files on the side; if it is newly installed, there should be no files on the side) : ![Image](VSCodeSS.png)
