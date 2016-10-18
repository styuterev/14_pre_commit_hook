# 14_pre_commit_hook

The program is used to solve quadratic equasions. It takes three arguments, that are coefficients A, B, C of an equation A\*x\*x + B\*x + C = 0. It returns two solutions, some of which may be None, if there is no solution in real numbers available.   

To prevent developers from infesting the code with bugs, tests and git hook are also provided. To install the hook, you need to create a symlink of it in a special hook directory. To do so, you need to type the following commands in terminal:

> cd .git/hooks/   
> ln -s ../../pre-commit pre-commit

After the hook is installed, every time you try to commit some changes, tests from __tests.py__ will be run. If at least one of them fails, your commit will be aborted, and you'll see the following message:

> "Tests didn't pass. Commit is not allowed."

In this case, you need to have another look at your changes and fix the bugs you've created.

If everything is fine, the commit passes, and the message will look like the following:

> "Tests passed. Commit is allowed."
