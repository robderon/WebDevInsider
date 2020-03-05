# LAB 1 SPEAKING HTTP

When you type a URL in the adress bar and press enter, the browser (the client) must ask for something , and a server must answer and send the requested content. HTTP is the language of this exchange.


If I type http://www.example.com/ and press enter :

1.  The browser sends a request line and request headers ( key:value pairs) : 
```HTTP
GET / HTTP/1.1
Host: www.example.com
Connection: keep-alive
...

````

2. The server answers with status line and response headers, then two line breaks, and the content, usually html

```HTTP
HTTP/1.1 200 OK
Content-Type: text/html;
...

<html>
<head>
...
</html>
```



---

HTTP HEADERS :
Information exchanged between client and server during a http request, in the form of name:value pairs. They include : name and version of the browser, cookies, Last modification date, duration of the cache, accepted languages, accepted file formats .... They are never displayed in the browser.

---

>1. install Netcat 

Linux : `sudo apt-get install netcat`

( if it's the first time you are using apt-get you should do `sudo apt-get update` before)

Mac : `brew install netcat`

>2. Run netcat as a server

In a shell, run netcat in listen mode on port 9502 :

`netcat -l -p 9502`
or `nc -l -p 9502` depending on your version. 

>3. Connect to the netcat server 
go to  http://localhost:9502 with your browser. Nothing will happen in the browser, it's normal. now go back to the netcat window. you should see the http request the browser sent to the server.
This is HTTP request, with request lines and request headers.

---

> run netcat in server mode again, connect with your browser using the same url, and this time, once the browser made his request, cut paste this text into the terminal window. See what happens.

````HTTP
HTTP/1.1 200 OK
Content-Type: text/html;


Hello World !
````

---

>  do the same with a request from your mobile phone (you must be on the same Network to do this, either with connection sharing, or when both your mobile and your phone are on the same wifi network ). You must know how to find your ip adress

# LAB 2 Static Web

1. Setup and run a static web server on the port you like

2. Create IMAGES directory and put an image from the web in it using wget

3. Create index.html in the root directory , with these tags : html, head, title, body,  p, h1, h2, a href, ul, li, img. index.html must contain and image and a link to faq.html

4. Create FAQ/faq.html containing a h1 title and a link to index.html

Directory structure should look like :

```
/index.html
/FAQ/
/FAQ/faq.html
/IMAGES/
/IMAGES/xxxxxxxx.jpg
```

5. Request the website from your browser.

6. Request the website from your mobile phone

help:   https://www.w3schools.com/html/html_intro.asp


# Lab 3 Basic Styling


1. Use Adobe color to find a color palette.

2. Give default style to all your html tags using a css external file. Your css will include element selectors for all the tags of the <body></body> part of your page

help:
https://www.w3schools.com/css/css_intro.asp

https://www.w3schools.com/css/css_selectors.asp

https://internetingishard.com/html-and-css/

# LAB 4 Responsive Design

### PART 1

1. Add a h1 title on the home page : "Web Architectures"

2. Add a about.html page with an image in it.

3. Add a navigation menu bar with 3 buttons : Home, Faq, About. The menu should be horizontal on large viewport, and vertical on small viewport.

4. Images on the index and about page should be centered , and take the full width of the page, without exceeding their original width.

5. Use the chrome developper tools to show screen size selector and verify your design.

6. if your phone and your computer are on the same network, try requesting your server with your phone to confirm good responsive design.

Help : https://www.w3schools.com/html/html_responsive.asp

----
### PART 2

1. Sur la page faq créez un `<div></div>` contenant un `<p class="question"></p>` et un `<p class="reponse"></p>`

2. Rédigez une question et un réponse en rapport avec le cours

3. Créez encore 2 divs sur le même principe avec question / réponse ( crééz du contenu utile)

4. Créez un formulaire en bas de la page faq avec un champ question, un champ réponse et un bouton submit.

5. Les labels sont affichés à l'intérieur des champs.  utilisez `onfocus=` pour effacer le contenu dès qu'on clique dans le champ.

6. Le contour des champs change de couleur quand le champ est actif

Help: https://www.w3schools.com/html/html_forms.asp

pour associer du code JS aux évènements de la page :
https://www.w3schools.com/js/js_htmldom_events.asp

# LAB 4 LET’S GET DYNAMIC

1. Créez un dossier `cgi-bin/` dans votre document root , et placez y un script appelé hello.py contenant le code suivant :

```PYTHON
#!/usr/bin/env python3

print("Content-type: text/html")
print("")
print("""
<html><body>
<p>Hello World! </p>
</body></html>
""")

```

( La première ligne est importante, c'est grace à elle que Linux va savoir comment éxecuter ce script. en l'occurence, lancer python3. Contrairement à windows, l'extension ne signifie rien sur Linux, elle n'est la que pour vous donner une indication)

2. toujours dans le dossier cgi-bin, tapez `chmod +x ./hello.py` pour rendre le script executable

3. Retournez dans le Document root directory avec `cd ..`, et lancer un serveur web python3 avec execution cgi : 
`python3 -m http.server --cgi 8503``

4. Saisissez l'adresse suivante dans votre navigateur:
http://localhost:8503/cgi-bin/hello.py