# Entry 4 - Making my project functional
### 03.20.23

#### The separate pages
When working on this project, I mapped out the two main goals that complete the MVP. Aside from the pure function of the app, of adding, deleting etc. to a list, I also had to figure out how to make multiple pages and connect each of these pages to the home screen. Once that connection is established, I can begin working on the details / functions of the data collection and printing to the different created views. <br>
#### Navigation method <br>
After researching possible methods that can connect to the different views, I knew I wanted to be able to traverse through each of the views and also be able to return to the home screen to go to other views. The method that fit this style ended up being the `NavigationView`. This view allowed looking through different views with an animation style that is like swiping through something. It also lets the user navigate back to the main screen / first view by clicking the top left corner, where an arrow takes you back to the initial screen.
The basic code for my specific project is shown here (prior to any design implementation) <br>
<img width="429" alt="Screenshot 2023-04-17 at 11 19 35 AM" src="https://user-images.githubusercontent.com/73554006/232534126-27dd1114-5649-4367-b0a8-483884902ba9.png"> <br>
Going through it, the top is what creates the overall Navigation style view. Once created, I placed the application logo and buttons into a vertical stack that ensures it is organized on the screen. Then, the button in the screen called the `NavigationLink` is what I will be using to move through the views. <br>
**Explaining NavigationLink** <br>
<img width="358" alt="Screenshot 2023-04-17 at 11 46 04 AM" src="https://user-images.githubusercontent.com/73554006/232539931-3ec0c5f0-73bc-4f5d-bf1e-fa234392ac6e.png"> <br>
The label, like a button, is what is presented, for example here we will see 'Add to List' with a blue color to represent that clicking it will take you somewhere. The destination is the actual name of the page, here called  `AddList()`. When we click the button, it is *calling* the other view to come and take the place of the original view. <br>
#### Successes
Using this method was very successful, and I was able to create the basic movement between screens that is one of my main pieces of my project. The code above creates this home screen below. <br>
<img width="335" alt="Screenshot 2023-04-17 at 11 55 26 AM" src="https://user-images.githubusercontent.com/73554006/232542706-b049fcc0-0f55-4dcb-bdc4-07f328b5b8b1.png"> <img width="311" alt="Screenshot 2023-04-17 at 11 55 36 AM" src="https://user-images.githubusercontent.com/73554006/232542818-b2f52588-b7cd-43f6-83a0-935f3aefd87d.png"> <br>
(Prior to adding the functions and style to the separate pages) Shown above is how with one click we start at the home screen and then we see the text , which I used as a placeholder to show how it went to the see list pages. I repeated this function with the other buttons and they work the same. The simple process is: 
1. The user opens the app to the home page
2. The user presses one of the buttons which leads to the view switching 
3. The user returns to the home page using the arrow at the top left <br>
#### My MVP plan - Understanding the functionalities <br>
Once I completed making the overall navigation function of the application, all that was left was the pure logistics of each screen. Using my [MVP Plan](https://docs.google.com/document/d/1-aWjIdviVXkR4k31HKN_4qVQc7dfO9_cn24f55OzP0o/edit?usp=sharing), this places me at at around 45% since almost half of the project is finished and completed. <br>
My next focus is on figuring out how to input all the functions of adding lists. Remembering my older project, I know that I need to grab data from a user and print it out, except this time I have to transfer it between views in the same application rather than passing the data to a completely different site. My plan is to figure out how to pass data, once I can nail that down, I expect the other logistics of printing out the data and managing it will come much easier. <br>
#### Where I am now + Goals and EDP <br>
In the **E**ngineering **D**esign **P**rocess, I find myself in between steps 5 and 6. I have already created a part of the prototype, but I also have another part that I am still in the process of working on. To add, I also will be testing the first part I made over and over, especially to ensure it continues working properly with what I am adding to the MVP. <br>
For skills, I believe I mostly used skills of *problem decomposition*, and *how to read*
* In *problem decomposition*, it was mostly in the entire MVP in general. I decided to split the two main functions of the project into smaller tasks, such as getting the code, then the design elements, then the functions. Dividing the overall problem of this application makes it easier for me to work on and end up with a more successful product.
* *How to read* mostly came into play with the `NavigationView`. Since it was a specific XCode function, I had to do research on it. I didn't understand much from watching help videos so I had to look into forums and read into detail for the specific help I needed in order to make it work with my project. <br>

[Previous Entry](entry03.md) | [Next Entry](entry05.md)<br>
[Home](../README.md)
