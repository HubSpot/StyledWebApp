# StyledWebApp

Check it out at: https://boiling-bastion-10158.herokuapp.com/

_Note: Unlike with the Base Web App, you shouldn't fork and clone the code in this repo onto your machine. Instead, try to follow the instructions below, using the code in this repo as a reference._

## Part One: Adding Pages and Navigation
 
In this section, you’ll add additional pages to your app and create navigation for users to move through your app’s pages. . We’re going to use the example of a personal website today, but feel free to add whatever pages you’d like. 

#### 1. Create the pages
Navigate to the `pages` folder, which holds the html pages. Create a couple more pages — an about page and a projects page, by right clicking the `pages` folder, then “New file.” Type in your filename for each, then hit “enter.”

#### 2. Add content to the pages
You can see that your new pages are empty right now. Copy the content from the index page, then paste it into the other two pages. Feel free to change the title so you can see which page is which.

#### 3. Hook up the pages so they render

Head to your “start.js” file. This function below tells your app to render the index page when it gets a request for the app’s URL:
```app.get('/', function(request, response) {
  response.render('pages/index');
});
```
Use this as a model for the other functions. Your about page should render when the user types in the url `/about`, and should render the “about” page instead of the “index” page, and the same for your projects page. How would you modify your code to do that? If you need a hint, check out the code in this repo.

Once you're done, save your page and open up your terminal again. Type `heroku local web` to get your server running, and navigate to `localhost:5000`. You should still see the same page as before, but now add `/about` to the URL. You should now see your new about page render.

_Note: Remember that you can stop the server in your terminal by typing "control" "c"._

#### 4. Create a navbar

Typing in URLs isn’t the most user-friendly way to get around an app. Users would be much better off with a navigation bar, or navbar, with links that users can click to move from page to page. Let’s add one.

Since your navigation will be every page, let’s create it as a helper and include it in all the pages, the same way the header information is included. Right click on the `helpers` folder, then add a file named “navbar.ejs.” 

Inside of that file, start building the navbar. Use an `<ul>` tag, then a `<li>` tag inside for each nav item. Since it should link to another page, add an `<a>` tag inside. The `href` of the link will mirror the code in your `app.get` function in `start.js` — if the `href` of your index page is `/`, what should the other pages be?

If your HTML is a little rusty, that’s okay. Check out [this tutorial](https://www.tutorialspoint.com/html/) for some additional information. Or, search for your own HTML resources on the internet — there are many great ones out there.

#### 5. Include the navbar on your pages
Copy the “include” tag from the header and paste it inside of your page header. Then “head” with “navbar” — the name of your helper file. Save that file, head to your browser to test it out. Refresh the page, and you should see your new navigation. And if you click on the link, it should direct you to the appropriate page. 

All that’s left to be done is to include the navigation on each page of your app.

## Part Two: Styling your app
Okay, so you have your web app created, complete with navigation. You’re probably wanting to make it more visually appealing for visitors, right? Now you'll add styling to your app to make it look great, and then explore a few key resources we’ve already included in your app that you can take advantage of. 

Your project's CSS lives in the `main.css` file. If you don’t have much background with CSS, check out [this tutorial](https://www.tutorialspoint.com/css/). You can also do some research on Google for additional information and tutorials. 

Notice that in your `head.ejs` file, there's a link to a Google font called Poppins. Google fonts are a great way to make your app look professional and beautiful.

Notice that there’s also a link to Bootstrap. Bootstrap is a popular front-end component library. It has lots of tools to make creating responsive, mobile-first web pages easy. Your app imports both the Bootstrap CSS and the JavaScript. If there’s another component library that you’d like to use instead, feel free to swap it in.

Let’s incorporate Bootstrap into your app. Through this, you’ll also practice exploring documentation — a crucial skill you’ll want to develop for continuing to build your web app. Your app’s navigation could use some styling help. Let’s see what components Bootstrap has to help us out.

Go to [getbootstrap.com](https://getbootstrap.com/), and head to the Documentation section. Go to Components, then find Navs. Here you’ll find all sorts of tools to make your navigation look the way you want it to. You can see that by adding a few classes to each element of the nav, it can make your elements automatically look much better. Go ahead and add those classes to your app’s navigation. Save that file, then refresh your page and it should look much better! 

Bootstrap is full of tools like this to make your components look more beautiful and modern without a lot of styling work on your part. While we like working with component libraries, feel free to style your elements directly — do whatever is going to help you build an amazing web app.

Now you can keep adding content and experimenting with the styles. With a  little trial and error, you’ll create an app that looks just the way you want it to. Once again, if you run into any problems, we encourage you to Google your question — more than likely, there are other developers out there that ran into exactly the same problem as you did. Often, their solutions can point you in the right direction.

Feel free to spend some time now polishing your application. With practice, your app will look better and better. Good luck!

## Additional Resources
- An explanation of Node.js: https://codeburst.io/the-only-nodejs-introduction-youll-ever-need-d969a47ef219
- An explanation of Express.js: https://medium.freecodecamp.org/going-out-to-eat-and-understanding-the-basics-of-express-js-f034a029fb66
- An explanation of EJS: https://medium.com/@atingenkay/getting-started-with-ejs-28fe4a693e53
- HTML tutorial: https://www.tutorialspoint.com/html/
- CSS tutorial: https://www.tutorialspoint.com/css/
- Bootstrap documentation: https://getbootstrap.com/

