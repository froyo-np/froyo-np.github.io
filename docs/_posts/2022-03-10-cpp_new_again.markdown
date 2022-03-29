---
layout: post
title:  "Lets make cool stuff with C++ part 1"
date:   2022-03-10 13:28:49 -0800
categories: c++
---

# Hello C++
I love C++ - but I've been away for a long while! C++20 is out and looking good, so Im going to be building some experimental things here in the coming posts. I am specifically interested in C++20 (particularly modules), WebAssembly, and graphics/rendering in general. So! I'm starting with a simple templated vector (as in GLSL, not std::vector) library that I've been toying around with [here](https://github.com/froyo-np/imvec). Some things I like about it - 
1. Its immutable - unlike GLSL's vectors.
2. Its pretty compact, but has handy template specializations like .xy(), overloaded math operators, etc.
3. Its probably not the fastest, but it feels pretty clean, and nothing is virtual, so it should pack well.

For now, its all in a .hpp file, but I'll be experimenting with converting it to a c++20 module soon - this will have handy consequences like hiding all the gross macro's I generated to do the exhaustive swizzle interface specializations.

After that, I'm going to extend the experiment and simple SDF rendering library, again with templates & C++20 modules. SDF-style rendering is very cool, and pretty new to me. A *__FANTASTIC__* blog on the topic is [here](https://www.iquilezles.org/www/articles/raymarchingdf/raymarchingdf.htm).

Lastly - my ultimate goal is to get all that built for WebAssembly - I've experimented with this a bit via Clang, but so far all my C++20 module experiments seem to work, up until its time to actually generate an executable .wasm file...

Anyhow, thanks for reading - stay tuned if the above interests you at all!