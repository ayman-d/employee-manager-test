# Employee Manager



__Express.static() Options__  
We need to allow users to type just the page they want to load in the url bar without having to add the .html extension. To do this we add have to add some options to the express.static() method.[options list](https://expressjs.com/en/api.html#express.static).  
 There are two options you can use for this have express ignore files with a dot extension and match files by name. Second use the extenstions option and give it a list of extensions you want to ignore. Remember express looks in the static folder first for a file matching the url endpoint. If it finds one then it will use it in the response.

```js
const options = {
  dotfiles: 'ignore',
  extensions: ['htm', 'html']
}
```

__CORS__
CORS stands for cross origin resource sharing. When were working in development the express server doesn't refresh the client browser each time we make changes to the html css or javascript. We can use the live server extension in VSCode and code out the front end as were used to. However the default port for VSCode is 5000. To express this looks as if your comming from a completly different url. So we need our express app to accept urls request from different ports. To do this we are going to install cors an express middleware that will handle cross origin requests.  
__Install CORS Express Middleware__
```npm
 npm install cors()
```
__Using CORS In Your Express App__
```js
const cors = require('cors')
app.use(cors());
```
setup cors


__Node Environment Variables__
An environment variable are a way of giving your application instructions about where and how to run. The Node environment variables are embedded during the build time. So for the case of the server when it starts up. You could tell the server when it starts up if it is in product live on the internet or just in development. This way you can have different pieces of you app run while your developing. For instance maybe you have a different database for a production and development each with different access keys. So you could set a varible to tell your application what key to use.  
__.env file__
```node
PRD_DB_KEY=1234
DEV_DB_KEY=12
```


### Read and Write Files
-fs.readFile()
-fs.writeFile()

### GET Request API
- setting up routes