# CompareCheck
Do cross-branch compares work properly?

This is the MASTER branch.

I would have expected comparing Branch [One](https://github.com/gojimmypi/CompareCheck/tree/CompareBranchOne) to Branch [Two](https://github.com/gojimmypi/CompareCheck/tree/CompareBranchTwo) to work differently. Although branch two is selected on the left, the contents of the Master branch are actually being compared to Branch One on the right. 

See: https://github.com/gojimmypi/CompareCheck/compare/CompareBranchTwo...CompareBranchOne

![Image of GitCompare](https://raw.githubusercontent.com/gojimmypi/CompareCheck/master/GitCompare.PNG)

Perhaps I simply don't know how to do a cross-branch compare. Still, I opened a GitHub issue, as either this really is not working properly - or at least this will be a feature request to make it more intuitive ;) 

https://github.com/github/hub/issues/1691



