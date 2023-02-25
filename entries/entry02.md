# Entry 2 - Starting to learn my tool
### 12.19.22
#### Ideas for how I'll learn <br>
In the last blog, I had briefly mentioned how I was going to watch a few videos as well as review the documentation. Although that was a more general idea. I had the project created, as well as the connection between Github and Xcode already. However, I found myself, even after reviewing forums and looking briefly into some videos, I didn't have much of an idea of where to start on Xcode. To further my learning, I had to focus on one of the main methods I learned, which was visually. I researched on resources like Youtube for any helpful guides to get me started coding on Swift itself, and found a youtube series that I thought would be helpful if I coded along with the videos. This way the skills I was learning would also stick with me. <br>

#### Coding videos + Coding along with them <br>
The [series](https://youtube.com/playlist?list=PLMRqhzcHGw1Y5Cluhf7pKRNZtKaA3Q4kg) I found on Youtube allowed me to get started on Xcode, and fully familiarize myself with the library and how to form and also test code through experiencing it myself. <br>

##### What I made / learnt from the first video <br>
For each of the lessons in this mini series, I often watched each video twice. Once for general notes and getting what I was learning in my head, the second time usually to review any parts I didn't understand, as well as try out the code skills I learnt for myself. As I watched the video, I found it most helpful to take notes on a piece of paper of what was being told, except in a way I could understand. Then, as a way of review, I transferred these notes into my digital notes. After the first watch of the video, this is often what I was left with: 

(snippet of notes using the final notes from the first video of the lessons)
<img width="637" alt="note snippet blog 2" src="https://user-images.githubusercontent.com/73554006/221331017-6238bd46-843b-474e-b284-28533cb8c097.png">

Then for the second watch, I would usually play the code along portions of the video lessons and work along with them so that I could get hands- on experience coding on Xcode. For example, the point of the first video was introducing the library, which a lot of the code elements (such as stacks, font elements etc) I'll be using for my project will be in. In creating a sample app with these elements, I not only learned how to work with the library that comes in Xcode, I learnt how to create parts of my own future project (e.g, I would need having multiple stack elements in order to organize the different portions, such as text boxes, images, and buttons, properly on the screen). For the first video, I ended up with the following code: 
``` Swift
struct ContentView: View {
    var body: some View {
        ZStack {
            Color(red: 0.5, green: 0.5, blue: 0.5).ignoresSafeArea()
            VStack {
                Image("cat")
                    .resizable()
                    .cornerRadius(40.0)
                    .aspectRatio(contentMode: .fit)
                    .padding(3)
                Text("This is a cat")
                    .font(.largeTitle)
                    .fontWeight(.heavy)
            }
        }
    }
}
```
Which created the following: 

<img width="546" alt="cat view coding" src="https://user-images.githubusercontent.com/73554006/221331435-c41d1f14-7c35-4100-8f5e-d744db83ca8e.png">

Although it does not appear like much, this code had a lot of parts in it that were important to learn. As I mentioned before with the different stacks that organize elements for the UI, having a Vstack inside of a Zstack allowed for the grey background to actually appear as a grey background. Otherwise, it would appear in front of the cat image and text box, covering the entire screen. Furthermore, the Vstack itself organized the image and text vertically instead of on top of each other. Modifiers seen under the image and text (resizable and corner radius etc) were for the UI as a whole, and to ensure it all looked good. The resizable screen made sure the image looked good on each screen no matter the size, and something like `.ignoresSafeArea()` is to make sure the colored background fills in the top and bottom spaces on a mobile device. Doing these codes along with lessons each time allowed me to learn more and more about my Swift tool, which would then prepare me for the making of my book application. <br>

#### Using a resource from the summer <br>
Along with the youtube lessons, I also found myself planning to use a resource from the summer. In searching for hands-on coding experiences, I found that code academy had a few free lessons about using Swift and Xcode, and I planned on also working on those lessons so that I could further learn how to use Swift at its maximum capacity and get the best final product MVP for my project. <br>

#### Next steps <br>
My next steps after finishing reviewing the videos are to start on code academy lessons just to have that extra boost in confidence that I know what I am coding with. Then, I plan on working on some initial parts of my code, just to test out and see how my app could work in Xcode. <br>

#### Where I am / Skills <br>
In the **E**ngineering **D**esign **P**rocess, I find myself to be in between steps 3 and 4. Although I think I am planning on the best way to approach starting my project, I still find myself preparing by learning my tool, and in this preparation, I feel I am still brainstorming possible solutions of my project. As for skills, I feel I have used the skills of *Organization* and *Logical reasoning*. <br>
* In *Organization*, the system I created for myself in fully understanding all the concepts I was being taught in the videos required me to organize my thoughts. Using pieces of paper, I first got my initial thoughts, and then I moved them into a more organized digital notes, that in the future I could also use as a resource for anything that may confuse me in the future. 
* Going side by side with organization, I used the skill of *Logical reasoning* in understanding what I was learning, and implementing in example code. A lot of what I was being taught, I often put it in my own words so I could understand it better, which often called for me using my own reasoning to make connections. Using this reasoning is what I often relied on when coding along. Instead of copy pasting from the screen, I used my own understanding and logic to recreate the code being taught to me. <br>


[Previous Entry](entry01.md) | [Next Entry](entry03.md)<br>
[Home](../README.md)
