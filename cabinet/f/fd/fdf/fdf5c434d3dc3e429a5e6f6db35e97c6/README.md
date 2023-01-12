# Removing Punctuation

- Use `sed` to remove punctuation from lines:
	- From beginning: `sed 's/^[^[:alpha:]]\+//' {file}`
	- From end: `sed 's/[^[:alpha:]]\+$//' {file}`
- A list of punctuation useful to tokenize a sentence include:
```
. ! ? , ; :
```
- See also: [Removing Smart Quotes](../../../../c/c4/c48/c48ff3fd415dadc0d524b473f883fdb9/)
