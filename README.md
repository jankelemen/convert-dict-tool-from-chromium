This repo contains binaries compiled for Linux, which are necessary to run `convert_dict`. `Convert_dict` is a tool that compiles hunspell dictionary files (`.dic`, `.aff` and `.dic_delta`) into one binary `.bdic` dictionary, which Chromium based browsers use for spell checking. All the binaries combined are around 153MB

You can learn more about `.dic`, `.aff` and `.dic_delta` files [here](https://www.chromium.org/developers/how-tos/editing-the-spell-checking-dictionaries)

# How to generate `.bdic` dictionary

- Make sure that `convert_dict` binary is executable (use `chmod +x`)
- Place `.dic` `.aff` and `.dic_delta`  into the same folder (I recommend putting it in the folder where the binaries are) and make sure those 3 files have the same name, e.g.:
```
foo.dic
foo.aff
foo.dic_delta
```
Then run this command:
`$ path-to-convert_dict path-to-hunspell-files/name-of-those-files`
So, for example, if those 3 files are named `foo` and are placed in the same directory as the binaries, run:
`$ ./convert_dict foo`

---

If you're interested in Slovak dictionary without accents (diacritics) for Chromium based browsers, you can check that out [here](https://github.com/jankelemen/sk-ascii-dictionary-for-chromium)
