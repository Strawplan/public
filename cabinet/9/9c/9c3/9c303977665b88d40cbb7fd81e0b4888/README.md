# Wikipedia

- To copy text from Wikipedia without the references open the ‘Developer Tools’ (`Ctrl-Shift-I`) and enter the following into the console :
```
javascript:document.querySelectorAll('.reference').forEach(r => r.remove())
```
- This can be made into a [Bookmarklet](../../../../5/57/572/57246a7d2ae8211686940f6264067f9f/) if needed.
