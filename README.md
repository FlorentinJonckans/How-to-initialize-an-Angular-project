<h1 align="center">Guide to initialize an Angular project</h1>

<h2>How to initialize an Angular project</h2>

First of all, this guide is for people working on a Linux environment.

<h3>1 - Install <a href="https://angular.io/cli">Angular CLI</a></h3>

Install the Angular CLI by using the npm package manager:

`npm install -g @angular/cli`

<h3>2 - Create the initial base of an Angular project</h3>

After installing your Angular Cli, you will finally be able to create the beginnings of the creation of your first [Angular](https://angular.io/docs) project.

To start with, you will have to create your Angular project :

`ng new mon-application-angular`

This line of code is the so-called classic way to create an Angular project.

There is also a command that allows you to create an Angular project, however, you create it using SASS (Syntactically Awesome Style Sheets):

`ng new mon-application-angular --style=scss`

<h3>3 - Test your project</h3>

Before testing your project, you must first go to the root directory of your project:

`cd my-angular-app/`

And then, you will have to build your application and serve it locally, the server automatically rebuilds the application and reloads the page when you change any of the source files.

`ng serve --open` or just `ng serve`

If you've followed everything so far, your terminal should send you to a local server to preview your application.

For example: `http://localhost:4200/`

<h3>4 - Create your first <a href="https://angular.io/api/core/Component">component</a> in your project</h3>

Before adding a component to your project, you must be sure to be at the root directory of your project.

Then, to create your first component you will have to use:

`ng generate component component-name`

This line of code can be simplified by:

`ng g c component-name`

Here is an example of creating a component : `ng g c about`

<h3>5 - Root the component</h3>

We are now going to move on to a complicated part of an Angular project, the [routing](https://angular.io/guide/router).

First, move through your folders to find the `app-module.ts` file:

`cd src/app/app-module.ts`

You will have to import your component that you created earlier in your `app-module.ts` file and then, add informations about your [@NgModule](https://angular.io/guide/ngmodules):

```js
import { AboutComponent } from './about/about.component';

   @NgModule({
       declarations: [
         AppComponent,
         AboutComponent
       ],
       imports: [
           BrowserModule,
           AppRoutingModule,
           RouterModule.forRoot([
      {
        path: 'about',
        component: AboutComponent
      }
      ])
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

<h3>6 - Check the rooting if it's working</h3>

You've done a great job so far but don't quit this help right away, you have to make sure that the routing is working correctly.

Go to the directory where the `app.component.html` file is located and add: 

```html
<nav></nav>
<div class="main-content">
  <router-outlet></router-outlet>
</div>
<footer></footer>
```

Thank you for following this guide until the end, do not hesitate to share this guide if you liked it and follow me.





