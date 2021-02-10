---
layout: post
title:      "Binary Tree"
date:       2021-02-10 16:34:19 -0500
permalink:  binary_tree
---

```
      1
   /      \
  2       2
 / \      / \
3  4  4  3
```


Above is a binary tree, a data structure which has one root value that branches into two or less children. Typically, the children are named left and right. 

In ruby, the creation of a tree looks like so:
```
 class TreeNode
     attr_accessor :val, :left, :right
     def initialize(val = 0, left = nil, right = nil)
         @val = val
         @left = left
         @right = right
     end
end
```

Once created, manipulation becomes easy as things are labeled clearly: there will be the root element and then the left and right children that respond via dot notation. Thus, if looking at the tree above, to access the elements '2', root.left or root.right will work.
