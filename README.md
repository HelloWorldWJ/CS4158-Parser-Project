# CS4158-Parser-Project

Jian Wang - 20125984

## Part1 The Lexer
### [Steps] The build and execution for my lexer

flex lexer.l

gcc lex.yy.c

./a.out

(You can then test the example by typing from the keyboard.)


### Screenshots
The following are some screenshots of running examples.

![image](https://user-images.githubusercontent.com/43991412/159789581-84bf37da-7a04-4a72-8775-202171cbb1c9.png)

![image](https://user-images.githubusercontent.com/43991412/159789621-3b177b3c-ded9-4c2f-bb35-768916825704.png)

![image](https://user-images.githubusercontent.com/43991412/159789698-0365a511-4e6f-45e3-9459-4b849a77e7e4.png)

![image](https://user-images.githubusercontent.com/43991412/159789755-5db67bc7-e1de-4959-9357-9dc9da04f4f6.png)

![image](https://user-images.githubusercontent.com/43991412/159789795-f330724c-988b-4436-b124-a8e1a920910c.png)

![image](https://user-images.githubusercontent.com/43991412/159789821-2fcdc6ec-c79e-4b9a-aa7b-2b4d945424e0.png)

![image](https://user-images.githubusercontent.com/43991412/159789851-a610a57a-f611-4894-8397-86b7e5883789.png)

![image](https://user-images.githubusercontent.com/43991412/159789887-0ac75d54-466f-4797-be9f-3622f0516b68.png)

![image](https://user-images.githubusercontent.com/43991412/159789928-d0e792b3-3eb4-42fd-8f71-6fcc53e72cb1.png)

![image](https://user-images.githubusercontent.com/43991412/159789945-330c01ec-b782-4bbb-b816-e3b562e47874.png)

![image](https://user-images.githubusercontent.com/43991412/159789966-d548be8f-ec41-4e40-930e-99075b5d04e2.png)

![image](https://user-images.githubusercontent.com/43991412/159790013-7a138833-0e60-4962-9dc1-1fa89182f1ac.png)


## Part2 The Full Parser
### Note
This parser allows the program text to be only BEGINING and END, with no declarations or statements between them
### Something that may cause you confusion
![image](https://user-images.githubusercontent.com/43991412/165846315-4e9339d9-0b31-4df3-bc23-2b46ce62cb2b.png)

When a program is **not well-formed**, the parser exits on the line where the error statement appears. If typed in by pasting text, the content following the line of the error statement will automatically appear on the command line and run. For example, the statement on line 13 (the space) in the diagram above has been run as a command in the terminal.

### [Steps] How to run it
#### Method 1:

flex lexer.l

bison -d parser.y

gcc lex.yy.c parser.tab.c

./a.out

#### Method 2:

flex lexer.l&&bison -d parser.y&&gcc lex.yy.c parser.tab.c&&./a.out

