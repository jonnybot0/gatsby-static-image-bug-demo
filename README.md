This site demonstrates [a bug](https://github.com/gatsbyjs/gatsby/issues/8479) with Gatsby in which
images from the static folder aren't properly prefixed. 

To demonstrate the error, just run the `demoprefix` script in package.json (e.g. `yarn demoprefix` or `npm run demoprefix`).
That should build the site and start serving it at http://localhost:9000/path/to/my/site/.

You'll notice that the SUCCESS.jpg image fails to load. However, if you navigate to 
http://localhost:9000/path/to/my/site/img/SUCCESS.jpg,
you'll see that the image is there.

It fails because the image path the site uses is http://localhost:9000/img/SUCCESS.jpg, which is wrong.

This site is based on the [Gatsby MDX starter](https://gatsby-starter-mdx-basic.netlify.com/), 
but the bug probably affects other, non markdown/MDX based Gatsby sites as well.

This starter build MDX support into the
[gatsby-default-starter](https://github.com/gatsbyjs/gatsby-starter-default). Its README also applies here.
