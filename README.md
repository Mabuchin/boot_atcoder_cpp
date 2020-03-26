# boot_atcoder_cpp

atcoder-cli usage : [http://tatamo.81.la/blog/2018/12/07/atcoder-cli-tutorial/](http://tatamo.81.la/blog/2018/12/07/atcoder-cli-tutorial/)
online-jadge-tools usage : [https://online-judge-tools.readthedocs.io/en/master/introduction.ja.html](https://online-judge-tools.readthedocs.io/en/master/introduction.ja.html)

### 1. Open dev container with vscode
### 2. Login with atcoder-cli
```
$ acc login
```
### 3. Fetch the contest
If you want to fetch abc140/A, 
```
$ acc new abc140 --template cpp
```
Select problem A
```
$ cd abc140/a
```
### 4. Write a code & Compile it

```
$ vim main.cpp
$ g++ -std=gnu++1y -O2 -I/opt/boost/gcc/include -L/opt/boost/gcc/lib -o ./a.out ./main.cpp
```
### 5. Run the test
```
$ oj t
```
### 6. Submit the code
```
$ acc submit
```
### 7. Add another problem.
```
$ cd ../
$ acc add --template cpp
```

## Edit templates

```
$ vim .config/atcoder-cli-nodejs/cpp/main.cpp
```
