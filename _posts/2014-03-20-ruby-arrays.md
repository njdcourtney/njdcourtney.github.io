---
layout: default
title: Convert single items to arrays
tags: programming, ruby
---

This is one of those, "I keep losing this snippet, so I'm going to write it down" posts.

In Ruby, I often find myself writing methods that take Arrays to Emunerate over. There's a neat trick you can do using the Splat operator to convert a single item into an Array.

<pre>
# [*items] converts a single object into an array with that single object
# of converts an array back into, well, an array again
[*items].each do |item|
  # ...
end
</pre>

Neat!

This is a very old trick that I picked up from [this post on Ruby Inside](http://www.rubyinside.com/21-ruby-tricks-902.html) back in 2008, it's number 18.
