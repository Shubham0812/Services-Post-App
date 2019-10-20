
# Services - Posts-App

Services for Posts-Application also deployed on Github.

You can find the application [here.](https://github.com/Shubham0812/Posts-App)


## Technologies Used
- Node.js
- Javascript
- Express
- Mongoose


	#### Models

		Posts 
		title: string
	    content: string
	 

## How to use?

 #### Prerequisites
 - An active internet connection.
 - Node & Npm.
 - Visual Studio Code.

#### Usage

1. Download or clone the repository.
2. cd into the directory.
3. Install the required dependencies using `npm-install`.
4. To start the server locally use  `node server.js` .


#### Requests

The following requests are supported by the server.

	1. GET 	 ("/api/posts")
	2. POST  ("/api/posts")
	3. DELETE ("/api/posts/postID")
	4. PUT ("/api/posts/postID")


## Code Sample

    app.route("/api/posts").post((req, res, next) => {
	    const post =  new Post({
			title: req.body.title,
		    content: req.body.content,
	    });
	    post.save().then(saved => {
	    console.log('ID', saved)
	    res.status(201).json({
		    message: 'Post API successfully called',
		    id: saved._id,
		    })
	    })
	})

## Credits

**©** **Shubham Kumar Singh** | *2019*

