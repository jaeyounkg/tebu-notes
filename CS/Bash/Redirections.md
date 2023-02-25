```bash
echo test > afile.txt
```
redirects stdout to afile.txt. This is the same as doing
```bash
echo test 1> afile.txt
```
To redirect stderr, you do:
```bash
echo test 2> afile.txt
```
& is the syntax to redirect a stream to another file descriptor - 0 is stdin, 1 is stdout, and 2 is stderr.

You can redirect stdout to stderr by doing:
```bash
echo test 1>&2 # or echo test >&2
```
Or vice versa:
```bash
echo test 2>&1
```
So, in short... 2> redirects stderr to an (unspecified) file, appending &1 redirects stderr to stdout.

(From the legendary StackOverflow answer [here](https://stackoverflow.com/a/818265))