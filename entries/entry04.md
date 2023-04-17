# Entry 4 - Making my project functional
### 03.20.23

#### The separate pages
When working on this project, I mapped out the two main goals that completes the MVP. Aside from the pure function of the app, of adding, deleting etc. to a list, I also had to figure out how to make multiple pages and connect to each of these pages to the home screen. Once that connection is established, I can begin working on the details / functions of the data collection and printing to the different created views. <br>
#### Navigation method <br>
After researching possible methods that can connect to the different views, I knew I wanted to be able to traverse through each of the views and also be able to return to the home screen to go to other views. The method that fit this style ended up being the `NavigationView`. This view allowed looking through different views with a animation style that is like swiping through something. It also lets the user navigate back to the main screen / first view by clicking the top left corner, where an arrow takes you back to the initial screen.
The basic code for my specific project is shown here (prior to any design implementation) <br>
<img width="429" alt="Screenshot 2023-04-17 at 11 19 35 AM" src="https://user-images.githubusercontent.com/73554006/232534126-27dd1114-5649-4367-b0a8-483884902ba9.png"> <br>
Going through it, the top is what creates the overall Navigation style view. Once created, I placed the application logo and buttons into a vertical stack that ensures it is organized on the screen. Then, the button in the screen called the `NavigationLink` are what I will be using to move through the views.
##### Explaining NavigationLink <br>
<img width="358" alt="Screenshot 2023-04-17 at 11 46 04 AM" src="https://user-images.githubusercontent.com/73554006/232539931-3ec0c5f0-73bc-4f5d-bf1e-fa234392ac6e.png">
The label, like a button, is what is presented, for example here we will see 'Add to List' with a blue color to represent that clickign it will take you somewhere. The destination is the actual name of the page, here called  `AddList()`. When we click the button, it is *calling* the other view to come and take the place of the original view.<br>
#### Successes <br>
Using this method was very successful, and I was able to create the basic movement between screens that is one of my main pieces of my project. The code above creates this home screen below. <br>
<img width="335" alt="Screenshot 2023-04-17 at 11 55 26 AM" src="https://user-images.githubusercontent.com/73554006/232542706-b049fcc0-0f55-4dcb-bdc4-07f328b5b8b1.png"> <img width="311" alt="Screenshot 2023-04-17 at 11 55 36 AM" src="https://user-images.githubusercontent.com/73554006/232542818-b2f52588-b7cd-43f6-83a0-935f3aefd87d.png">

#### My MVP plan
#### Understanding the functionalities - Plan
#### Where I am now + Goals and EDP
[Previous Entry](entry03.md) | [Next Entry](entry05.md)<br>
[Home](../README.md)
