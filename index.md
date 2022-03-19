# My first meme created

## Introduction 
Hi guys I'm currently taking a very interesting course named **stats220** data technoology, If you are interested please come to our [course introduction page ](https://courseoutline.auckland.ac.nz/dco/course/STATS/220/1213)

### some idea about the meme
study at home is always a really hard thing. I always feel tired when i'm studying. That's the main idea about the meme. The cute cat picture came from tiktok and it's good for private use and it's reallyyyyyy cute! For the pigeon, there is a colloquialism called "放鸽子"(fang ge zi) From the word it means release the pigeon but Chinese people says that when people make a promise but not keeping it. The word "GUUUderbye" is because in China people say the sound of pigeon is 咕（Gu) So more people uses Gu to replace 放鸽子.  Hope you can get what I mean!



![my_meme](https://user-images.githubusercontent.com/101080556/159102596-6c1b04fc-3324-47da-afaa-28b19c89b71a.png)

And this is my R code
library(magick)

pigeon1 <- image_read("https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTpwmV0exiEKxGR_zlah9tQINbrkaU3yXif2w&usqp=CAU")%>% image_scale("281") %>%  image_annotate(text='GUUDER~BYE!',size=40,color='#00D7FF')



text1 <- image_blank(width=500,height=173,color='#C7B5C7') %>% image_annotate(text='When people\nask you\nto study',color='#B4ABD8',size=60,gravity = 'center')


m1 <- image_read('https://scontent.fnpe1-1.fna.fbcdn.net/v/t39.30808-6/275938189_1416724942080044_2966838335972489886_n.jpg?_nc_cat=103&ccb=1-5&_nc_sid=5b7eaf&_nc_ohc=00m9Frb8QbwAX_ruDIX&_nc_ht=scontent.fnpe1-1.fna&oh=00_AT9DvpSvuCNu2Xe6XKr6nO8c43YztpB3HuEMIb-82jlf9g&oe=623A4F53') %>% image_scale("x500") 

text2 <- image_blank(width=500,height=500,color='#C7B5C7') %>% image_annotate(text='When you \nare free',size=80,color='#F800FF',gravity='center')

row1 <- c(m1, text2) %>%
  image_append()

row2 <- c(pigeon1, text1) %>%
  image_append()

meme <- c(row1, row2) %>%
  image_append(stack = TRUE)

meme



image_write(meme, "my_meme.png")
