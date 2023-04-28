# Entry 5 - Setback and final project
##### 04/17/23

#### A big bug <br>
A major update from my project was once I had created the separate pages, I needed to look into how to *pass data between screens*. Since my own knowledge of this didn't have any idea on how to do this, I began researching videos and tutorials. A difficult part of this was that a lot of videos were very old and were using methods from different versions of XCode, which made it very difficult for me to follow along. After enough searching, I decided to watch one tutorial video in order to learn from it and try to implement certain methods into my code. However, once I finished I came across a bug that did not allow for the app to work, or even be tested. The difference with this error compared to other errors I had was this one was in the framework that came with the project and allowed Xcode to even run in the first place. Because of this, and after days of trying to debug and work through the code, I realized I would have to restart my project from scratch in a new file. <br>
#### Having to restart <br>
With restarting, I also took the opportunity to set up the proper file. One of my major problems when researching help videos for transferring data between viewcontrollers was that they were using different methods that were not available to me because, when I initially started my file, I made it multiplatform. A lot of the data transfer for Xcode is done with *mobile* only. Although I recognize that there are methods to be able to implement data transfer for multi platform applications, the resources and time I needed to be able to find this was not available. I created a new file for my project and switched to a mobile application framework only so that I can implement the focal point of my projects function. <br>
#### Storyboarding <br>
One of the keys to being able to transfer data between screens, which I needed for my project to function, is **storyboarding**. <br>
<img width="483" alt="Screenshot 2023-04-28 at 1 06 53 PM" src="https://user-images.githubusercontent.com/73554006/235210594-358f4e32-0268-40a2-964f-f4c85aa684be.png"> <br>
As seen above in storyboarding, I can more easily design each screen for my project. Then, using segues, I can connect each separate screen together and tell the computer to move to the screen it is pointing to depending on the action. For my project, the setting I put was *when this button is clicked, move (show) the next screen*. That command is what the segue is controlling. With this method, I was more able to connect each screen and be able to move data more fluidly through the code. <br>
#### View controller one <br>
In designing my project, and considering that I had to restart, I grabbed the basic ideas of what I wanted to do, but changed them around. Rather than having a home screen, I went straight into the organized list. Then on that screen there would be a button when pressed that takes you to the adding function. In there you would enter the information regarding the book you're adding, and then you click the add button. Once clicked, it will go back to the first screen and add the information to present onto the list. Making this work, I had to create two *view controllers*, one that holds the list and one that shows where the user will input the data. This is what my first view controller code looks like (on the top) and on the bottom is what the output is. <br>
<img width="627" alt="Screenshot 2023-04-28 at 1 26 13 PM" src="https://user-images.githubusercontent.com/73554006/235214771-828484fe-4c2f-46bf-85b2-973c75417bd8.png"><img width="393" alt="Screenshot 2023-04-28 at 1 23 03 PM" src="https://user-images.githubusercontent.com/73554006/235214784-05c1e768-f381-4471-be64-bd13d640ae88.png"> <br>
It is a lot of code for a simple function because there are different parts that are needed to ensure things work properly. To highlight some of the important functions: <br>
```Swift
@IBOutlet var tableView: UITableView!
   var books = [String]()
```
First, we create an outlet which overall is for the computer to know where the data is going and coming from. We then have an array that will hold all the book titles(it will get printed as a list). <br>
```Swift
@IBAction func pressedAddBook(){
      let vc = storyboard?.instantiateViewController(withIdentifier: "addedBook") as! SecondViewController
      vc.title = "New Book"
      vc.update = {
         DispatchQueue.main.async{
            self.updateBooks()
         }
         self.updateBooks()
      }
   }
}
```
This is the key code that begins the process when the button is added. This will first call the storyboarding functions that move to the next screen while also updating the array through calling the `updateBooks()` function. <br>
```Swift
func updateBooks(){
      books.removeAll()
      guard let count = UserDefaults().value(forKey: "count") as? Int else {
         return
      }
      for x in 0..<count {
         if let book = UserDefaults().value(forKey: "book_\(x+1)") as? String {
            books.append(book)
         }
      }
      tableView.reloadData()
   }
```
Update books first removes any extra info that hasn't been saved or printed, then creates a count to keep track of how many books are in the array. Once the count is done, it runs through the array to append whatever book is in the added array which will then print. <br>
But, to actually get the count and the book info to append, we need the functions from the second view controller. This is what is key about storyboarding and both view controllers is that they work *together*. <br>
#### View controller two <br>
The whole code for view controller two (where you enter the book data) is seen on the top and on the bottom is what it looks like. <br>
<img width="869" alt="Screenshot 2023-04-28 at 1 41 45 PM" src="https://user-images.githubusercontent.com/73554006/235216951-9eda2c2b-f044-406a-9e98-7108a95b2b6d.png"><img width="334" alt="Screenshot 2023-04-28 at 1 23 13 PM" src="https://user-images.githubusercontent.com/73554006/235216967-afa044c5-3e23-4efd-b66b-cf837cc074e4.png"> <br>
To explain the basics of the code: <br>
```Swift
func textFieldShouldReturn(_ textField: UITextField) -> Bool{
        saveBookTitle()
        return true
    }
 @objc func saveBookTitle(){
         guard let book = field.text, !book.isEmpty else {
             return
         }
```
This code ensures that the text field has something in it, since we do not want to pass any empty data. Once it checks if there is something in the field, it calls the `saveBookTitle()` function to begin the process. (First, my code saves the data, and then it transfers it to the next screen. 
```Swift
@objc func saveBookTitle(){
         guard let book = field.text, !book.isEmpty else {
             return
         }
        
        guard let count = UserDefaults().value(forKey: "count")as? Int else{
           return
        }
        let newCount = count + 1
        UserDefaults().set(newCount, forKey:"count")
        UserDefaults().set(book, forKey:"book_\(newCount)")
          
        update?()
          navigationController?.popViewController(animated: true)
     }
```
This is what saves the data. It creates the count that we saw increment in the other viewcontroller, adds one for each save, and also creates keys such as new books and the title. The `update?()` is what calls the updating book functionality in the other code. <br>
#### How the connection works

#### Final application

#### Beyond MVP

#### Where I am + Goals and EDP

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
