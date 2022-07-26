# Note-Taker
<img src="images\Screenshot 2022-07-25 222030.png">
<img src="images\Screenshot 2022-07-25 222149.png">

[Deployable Link: https://snyh212.github.io/note-taker/](https://snyh212.github.io/note-taker/)

## Description
Note-Taker is a web application that uses node.js with express, which allows a user to save, delete and review notes they input.

## Technologies used

HTML, CSS, JS, node.js, express, bootstrap framework
On VS Code and GitBash

## Code and Functionality
### Here in server.js is the code to create the port and a static directory for the webpage-

```
const app = express();
const PORT = process.env.PORT || 3010;

app.use(express.urlencoded({ extended: true }));
app.use(express.json());

app.use(express.static("./develop/public"));
```

### These lines of JS create a directory route structured in HTML files-
```
app.get("/notes", function(req, res) {
    res.sendFile(path.join(__dirname, "./develop/public/notes.html"));
});
app.get("*", function(req, res) {
    res.sendFile(path.join(__dirname, "./develop/public/index.html"));
});
app.get("/", function(req, res) {
    res.sendFile(path.join(__dirname, "./develop/public/index.html"));
});
```
### And here is the code that listens for the port-
```
app.listen(PORT, function() {
    console.log("App listerning on PORT http://localhost:"+PORT);
});
```

## Contact Infromation

[E-mail: Snyh121@gmail.com](mailto:snyh121@gmail.com)  
[GitHub: snyh212](https://github.com/snyh212)  
[LinkdIn: Shmuel-Hoffman](https://www.linkedin.com/in/shmuel-hoffman-254b0223b?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3BS2rg0PtBTLeG2szT2ZbGmg%3D%3D)