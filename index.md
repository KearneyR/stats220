# Assignment 1
### My Meme
![](https://github.com/KearneyR/stats220/blob/e04461353937ad79a0f1f93c8b063986e63d6840/my_meme.png)

* I like using R but I don't like memes for the most part
* I do like the Simpsons though (*who doesn't*)

The inspiration for my meme was the scene from [season 5 episode 16](https://www.youtube.com/watch?v=ZeyUP4g3oAY)

**Meme description**
1. I don't have any ideas for memes but was ready to get this assignment done
2. Coming up with it was the hardest part of the assignment
3. I knew I wanted to use a Simpsons one and this one fit perfectly
4. Even though I don't like memes I like the assignment, it was novel and more interesting than a regular uni assignment

#### Here is the image I cropped for use in my code (click for source)
[![](https://i.redd.it/ck5bzpxk7al61.jpg)](https://www.reddit.com/r/MemeRestoration/comments/lymy5s/homer_simpson_backs_into_bushes_4000x4000/)
### Here is the code
```r
homer1 = image_read("C:/Users/Kearney/Desktop/Uni/2022/Sem 1/Stats 220/Assignment1/Images/homer1.png") %>%
  image_scale(400) %>%
  image_border(color = "black")

homer2 = image_read("C:/Users/Kearney/Desktop/Uni/2022/Sem 1/Stats 220/Assignment1/Images/homer2.png") %>%
  image_scale(400) %>%
  image_border(color = "black")

first_text = image_blank (width = 400, height = 301, color = "#FFFFFF") %>%
  image_annotate(text = "Starting \nassignment 1", color = "#FFFFFF", 
                 strokecolor = "#000000",  size = 55, font = "Impact", 
                 gravity = "center") %>%
  image_border(color = "black")

second_text = image_blank (width = 400, height = 310, color = "#FFFFFF") %>%
  image_annotate(text = "Having to \ncome up with an \noriginal meme", 
                 color = "#FFFFFF", strokecolor = "#000000", 
                 size = 50, font = "Impact", gravity = "center") %>%
  image_border(color = "black")

topim = c(homer1, first_text) %>%
  image_append()
bottomim = c(homer2, second_text) %>%
  image_append()
meme = c(topim, bottomim) %>%
  image_append(stack = TRUE)

image_write(meme, "my_meme.png")


```
