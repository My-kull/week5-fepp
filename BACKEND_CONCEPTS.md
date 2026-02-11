# Backend and Proxy Insights [Iteration8]

## 1

```javascript
jobSchema.set("toJSON", {
  virtuals: true,
  transform: (doc, ret) => {
    ret.id = ret._id;
    return ret;
  },
});
```

Answer: Converts Mongoose document into javascript JSON

## 2

```javascript
app.use(cors());
```

Answer: CORS allows restricted resources on the web page to be requested from another domain

## 3

```javascript
proxy: {
  "/api": {
    target: "http://localhost:4000",
    changeOrigin: true,
  },
},
```

Answer: Sets target port for api usage to 4000 and makes the proxy responsible for translating request and response to the correct IP:s
