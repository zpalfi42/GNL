<h1 align="center">Get Next Line</h1>
<h4>For this project we will have to do a function. This function will have to return a line (sequence of characters enden with "\n" or "\0") readed from a file descriptor</h4>

## 📖 Mandatory Part 📖

- **Prototype** : `char *get_next_line(int fd);`
- **Files** : [`get_next_line.c`](./src/get_next_line.c) [`get_next_line_utils.c`](./src/get_next_line_utils.c) [`get_next_line.h`](./include/get_next_line.h)
- **Authorized Functions** : [`read`](https://man7.org/linux/man-pages/man2/read.2.html) [`malloc`](https://man7.org/linux/man-pages/man3/free.3.html) [`free`](https://man7.org/linux/man-pages/man3/free.3.html)

<h4>Calling you get_next_line function in bucle will let you read all the content from a file descriptor line by line</h4>

## 💣 Adding Get Next Line to your project 💣

#### To add GNL in your project you should add this lines on your Makefile:

`LIBS_DIR	= libs`

`LIBS			= $(LIBS_DIR)/Get_Next_Line/get_next_line.a \`

`LIBS_HEADERS	= -I $(LIBS_DIR)/Get_Next_Line/include/ \`

#### Add in your `CFLAGS` rule:

`CFLAGS		= -Wall -Wextra -Werror -g $(LIB_HEADERS)`

#### Add in your `$(NAME): $(OBJ)`:

`$(NAME): $(OBJ) $(LIBS)`

`⠀⠀⠀⠀⠀⠀⠀⠀@$(CC) $(OBJ) $(LIBS) -o $(NAME)`

#### Add in your `%.o:%.c` rule:

`@$(CC) -c $(CFLAGS) -o $@ $^`

#### And last thing is to add a new rule:

`$(LIBS_DIR)/Get_Next_Line/get_next_line.a:`

`⠀⠀⠀⠀⠀⠀⠀⠀@make -C $(LIBS_DIR)/Get_Next_Line`

#### If you want to include your own libraries too:

`INC				= -I $("YOUR_INCLUDE_DIR") $(LIBS_HEADERS)`

`CFLAGS		= -Wall -Wextra -Werror -g $(INC)`

#### Anyway, I have some [`C templates`](https://github.com/Zsolt42/42_Cursus_zpalfi/tree/main/C_Templates) if you want to see more clearly how to do it 😄😄

## 💯 Mark 💯

<p align="center">
  <a align="center">
    <img src="./Addings/Mark.png">
  </a>
</p>
