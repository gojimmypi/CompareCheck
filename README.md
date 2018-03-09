# CompareCheck
Do cross-branch compares work properly?

This is the MASTER branch.

I would have expected comparing Branch [One](https://github.com/gojimmypi/CompareCheck/tree/CompareBranchOne) to Branch [Two](https://github.com/gojimmypi/CompareCheck/tree/CompareBranchTwo) to work differently. Although branch two is selected on the left, the contents of the Master branch are actually being compared to Branch One on the right. 

See: https://github.com/gojimmypi/CompareCheck/compare/CompareBranchTwo...CompareBranchOne

![Image of GitCompare](https://raw.githubusercontent.com/gojimmypi/CompareCheck/master/GitCompare.PNG)

Perhaps I simply don't know how to do a cross-branch compare. Still, I opened a GitHub issue, as either this really is not working properly - or at least this will be a feature request to make it more intuitive ;) 

https://github.com/github/hub/issues/1691

## UPDATE: awesome response from github support :)

This is the right place for your question! We don't use Issues for public facing questions, but we would love it if you would consider posting your question on our forum next time if the question is not urgent and not private:

https://github.community

Now to your question itself. As weird as it might seem, what you are seeing is actually expected behaviour when using GitHub's website to compare branches.

We show what's called a "three-dot diff" which is the difference between the latest commit on the HEAD branch and the last common ancestor commit with the base branch.

Here are the commits on the head branch CompareBranchTwo:

https://github.com/gojimmypi/CompareCheck/commits/CompareBranchTwo

Here are the commits on the base branch CompareBranchOne:

https://github.com/gojimmypi/CompareCheck/commits/CompareBranchOne

And their last common ancestor commit is commit f329afb, so our compare view is showing the change that was brought to CompareBranchTwo after commit f329afb, which is commit 30337cc, and this is what you saw in the compare view:

https://github.com/gojimmypi/CompareCheck/commit/30337cc6db008714b04573f0d6c5f2216af99502

We are aware that this can be confusing, and in your case it is particularly non-intuitive. Most people expect to see a "two-dot diff", which would show the changes between the two most recent commits on each branch.

Unfortunately there is no way to choose which diff to show on GitHub's interface.

If you'd like, you can merge the base branch back into the HEAD branch (merge CompareBranchOne into CompareBranchTwo). That updates the last common ancestor and would be more likely to show you what you're expecting to see there.

I believe our engineers are aware of this confusion, and they might consider expanding the feature in the future, but it's very hard to say if or when will this change take place.

Hope this helps clear things up and please let us know if you have any other questions.


## Posted to https://github.community as a feature request here:

https://github.community/t5/How-to-use-Git-and-GitHub/Branch-to-Branch-Compare-Compares-to-Master-Instead/m-p/4677#M1527


