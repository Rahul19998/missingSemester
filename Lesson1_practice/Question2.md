## Question
What does the -l flag to ls do? Run ls -l / and examine the output. What do the first 10 characters of each line mean? (Hint: man ls)

## Answer
When we do `ls -l`, we get following output.

```
total 4
-rw-r--r-- 1 rahul rahul    0 Oct 14 03:22 Lesson1.md
drwxr-xr-x 2 rahul rahul 4096 Oct 14 03:31 Lesson1_practice
```

First 10 characters are `-rw-r--r--`.
First we need to understand what the characters stand for and mean:
* `d` : It represents directory. present if listed item is directory otherwise not. Also known as *File Type Prefix*
* `r` : Read Access.
* `w` : Write Access.
* `x` : Execution access.

We need to break it down and explain it one by one.
1. `-`: This define whether the listed item is directory or not.
2. `rw-`: This defines read and write access but not the execute access.

Similarly we see the the behavior and understand it.

Now why three sets of `rwx`. We need to understand that each rwx defines the access rights for different types of user.
1. First set is for the Owner/User. It shows permission it have for current file or directory. Example here user has read and write access.
2. Second set is for a group. Members of assigned group is same. Only read access.
3. Third is for Other/ World. Others have only read access.

