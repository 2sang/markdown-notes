How to redirect cout to files? - [StackOverflow](https://stackoverflow.com/questions/10150468/how-to-redirect-cin-and-cout-to-files)

```c
#include <iostream>
#include <fstream>

int main()
{
    std::ofstream out("out.txt");
    std::streambuf *coutbuf = std::cout.rdbuf(); //save old buf
    std::cout.rdbuf(out.rdbuf()); //redirect std::cout to out.txt!
    std::cout.rdbuf(coutbuf); //reset to standard output again
}
```

Should reset buffer using cout.rdbuf(), will cause segfault otherwise.
