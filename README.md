Cache, Proxies, Queues
=========================

Name: Bhargav Jhaveri

Unity ID: bjhaver

### Screencast:

https://www.youtube.com/watch?v=i5jyzg5vHO4

### Setup

* Clone this repo, run `npm install`.
* Install redis and run on localhost:6379
* Open two new terminal tabs and exceute ``` node main.js ``` and ``` node proxy.js```


### Set/Get dictionary and An expiring cache

Go to the web-page:

This will be used to set the dictionary.
```
localhost:5000/set-dict
```
This will be used to get the dictionary value.
```
localhost:5000/get-dict
```


### Recent visited sites

Go to the URL: 

```
localhost:5000/recent
```

### Cat picture uploads: queue

Navigate to the project home.
And execute:
```
curl -F "image=@./img/morning.jpg" localhost:3000/upload
```
You can upload any images in the above manner.

To visit the uploaded images in the browser visit:
```
localhost:5000/meow
```

### Spawn/Destroy/List
Spawn:

```
localhost:5000/spawn
```

List-Servers:
```
localhost:5000/list-servers
```

Destroy:

```
localhost:5000/destroy
```

### Proxy Server:

Proxy server is running at port 5000 and delegates the request to one of the available servers spawned.
Current logic for delegation is round robin fashion.
