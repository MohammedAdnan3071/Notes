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


# Middleware in next 

NOTE : While only one middleware.ts file is supported per project, you can still organize your middleware logic modularly . Break out middleware functionalities into seperate .ts or .js files and import them into your main middleware.ts file.
This allows for cleaner management of route-specific middleware, aggregated in the middleware.ts for centralized control.By enforcing a single middleware file, it simplifies configuration, prevents potential conflicts , and optimizes performance by avoiding multiple middleware layers.

