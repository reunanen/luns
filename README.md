# Lexicographically Unambiguous Numbering Scheme (LUNS)

## The problem

You start to number things, for example files:

* `Document_v1.doc`
* `Document_v2.doc`
* ...

By the time you reach `v10`, you realize that as soon as you sort the filenames lexicographically,
or let your operating system or similar do that, the resulting order has nothing to do with
the chronological order of your versions.

## The solution

After `Document_v9.doc`, just name it `Document_v90.doc`. Next comes `Document_v91.doc`, and so on.
You get the idea. 

You will come up with the following scheme:

* `Document_v1.doc`
* `Document_v2.doc`
* ...
* `Document_v8.doc`
* `Document_v9.doc` *(not in Conservative Mode)*
* `Document_v90.doc`
* `Document_v91.doc`
* `Document_v92.doc`
* ...
* `Document_v98.doc`
* `Document_v99.doc` *(not in Conservative Mode)*
* `Document_v990.doc`
* `Document_v991.doc`
* `Document_v992.doc`
* ...
* ...
* `Document_v998.doc`
* `Document_v999.doc` *(not in Conservative Mode)*
* `Document_v9990.doc`
* `Document_v9991.doc`
* `Document_v9992.doc`
* ...

Now if you are very very farsighted, you can use the Conservative Mode, where you entirely skip
the numbers `9`, `99`, `999`, ..., which are marked with *(not in Conservative Mode)* above.
Why would you do that? Just because in some cases the order of `99` and `990` (or `99` and `991`, ...)
might not be what you would expect.

## Rarely asked questions

### Isn't this scheme terribly inefficient?

Yes, it is, because you don't use the number `10` for example. However, enter ALUNS (which is
like LUNS, but uses even the alphabet!):

Start from `1`. By the time you'd hit `10`, go to `A` instead. Continue with `B`, and so on, until
you hit `Z`. Then go to `Z0`, `Z1`, `Z2`, ..., `Z9`, `ZA`, `ZB`, ..., `ZZ`, `ZZ0`, `ZZ1`, `ZZ2`,
..., `ZZ9`, ... – You get the idea!

You can also use HLUNS, for hex-LUNS, where you don't go to `Z` but only to `F`. Or if you feel
adventurous, you can even use ÖLUNS, where you go to `Ö`! Note that ÖLUNS is not recommended
for beginners.

### Wouldn't it be much better to start numbering from, say, `001`?

Yes, it would. However, enter ELUNS (Extended Lexicographically Unambiguous Numbering System):

Feel free to start from `001`, so you can effectively use every number between `1` and `999` without
making the ordering ambiguous. After `999`, just go to `9990`, and so on. It is not difficult.

Note that if you started from `1` and not `001`, you can still after `9` (or after `8` in the
Conservative Mode) go to `900` (and then to `901`) or even `9000` (and then to `9001`), or so.
Or, if you realize already at `5` that eventually there will be lots of versions, why not next
go straight to `5000` (or `6000` for Conservative Mode), and then to `5001` and so on?

### Can I combine ALUNS with ELUNS?

Yes, you can.

### Can I use ALUNS or ELUNS or their combination in Conservative Mode?

Yes, you can.

### Can I start from `0` instead of `1`?

Yes, you can.

### What about 汉字LUNS, 漢字LUNS, or similar?

Sure, go ahead!

### Wouldn't I be much better off using a proper version control system instead?

In the example case, yes. But sometimes you need to number things without them being different versions
of the same document.

### Is this a joke?

Does it look like one?