# Wrap and Unwrap

- To unwrap a file use `tr` *e.g.* `< {file} tr '\n' '△'`
- Alternatively use `xargs` to compress all white space *e.g.* `cat {file} | xargs`
- To wrap a text file use `fmt`, and to use put one word on each line use `fmt -1 {file}`
```
cat {in} | xargs -0 | fmt -1 > {out}
```
- The -0 parameter for xargs is required in case of single quotes in the input
- 
- Also see: [Removing Punctuation](../../../../f/fd/fdf/fdf5c434d3dc3e429a5e6f6db35e97c6/)