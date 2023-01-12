# Calling Pandoc

The following is a short helper script in [Bash](../../../../3/32/328/3289ce78ea480de601aa63030195da93/) to call Pandoc. With no format passed the
output will default to `gfm` which is GitHub’s version of markdown with the
addition of ‘smart’ quotes. Passing `latex` will change the extension to `tex`.

```
#!

# xpandoc

# Build various formats with Pandoc
# Clean up source with
#   'markdown' output format

f="$(readlink -f "${1}")"
d="$(dirname "${f}")"
b="$(basename "${f%.*}")"
s="${d}/${b}"

if [ "$#" -eq 1 ]
    then to="gfm-smart"
    else to="${2}"
fi

fnm="${s}"; inp="${s}.md"

ext="${to}"

if [ "${to}" == "latex" ]; then ext="tex"; fi

if [ "${to}" == "gfm-smart" ]; then ext="md"; fnm="README"; fi

pandoc                          \
    --output="${fnm}.${ext}"    \
    --from=markdown             \
    --to="${to}"                \
        "${inp}"

fi

fnm="${s}"; inp="${s}.md"

ext="${to}"

if [ "${to}" == "latex" ]; then ext="tex"; fi

if [ "${to}" == "gfm-smart" ]; then ext="md"; fnm="README"; fi

pandoc                          \
    --output="${fnm}.${ext}"    \
    --from=markdown             \
    --to="${to}"                \
        "${inp}"

```