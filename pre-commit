#!/bin/sh

git stash -q --keep-index

python tests.py
tests_result=$?

git stash pop -q


if [ $tests_result -eq 0 ]
then
echo "Tests passed. Commit is allowed."
exit 0
else
echo "Tests didn't pass. Commit is not allowed."
exit 1
fi
