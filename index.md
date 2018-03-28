## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/elfcandy/Doc_Test/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.


[gcc user guide](https://elfcandy.github.io/Doc_Test/gcc_user_guide.md)

[TEST](https://elfcandy.github.io/Doc_Test/test.html)


### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2

#git使用总结


CC = gcc
LD = ld
CC_FLAGS = -c -g -O0
LD_FLAGS = -T
#-lc
LD_FILE = s.lds

#successfully ops:
#1> gcc main.c -Wl,-Ts.lds
#2> gcc -c -g -O0 main.c -Wl,-Ts.lds
#3> gcc -c -g -O0 main.c
#   gcc -o ./a.out -Wl,-Ts.lds ./main.o
#            (-Wl is Optional)


    # -Wall -Werror 
    # -fPIC

all:
	./generate_ld_file.sh ${LD_FILE}
	${CC} ${CC_FLAGS} main.c -o ./main.o
	${CC} -o a.out ${LD_FLAGS} ${LD_FILE} ./*.o

#below is error
#	${LD} ${LD_FLAGS}s.lds ./main.o -o ./a.out

clean:
	rm -rf ./*.o ./*.out ${LD_FILE}



### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/elfcandy/Doc_Test/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
