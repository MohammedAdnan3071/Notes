# Middlewares 

Middlewares are code that runs before or after your request handler
It is commonly used for things like 
1. Analytics
2. Authentication 
3. Redirecting the user



`import express from "express";
const app = express();

let requestCount = 0;

app.use(
    function middleware(req,res,next){
        requestCount++;
        next();
    }
);

app.get("/", (req,res)=>{
    res.send("Hello world");
});

app.get("/requestCount",(req,res)=>{
    res.json({
        requestCount
    })
})
 
 app.listen(3000);`


