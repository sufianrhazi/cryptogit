Instructions
============

1. Clone this repository.
2. `git checkout encrypted`
3. Inspect the README file and note that everything is unredable.
4. Run the following commands:
  * `git config filter.crypto.clean 'openssl des3 -salt -k hody2'`
  * `git config filter.crypto.smudge 'openssl des3 -d -salt -k hody2'`
  * `git config diff.crypto.textconv 'cat'`
  * `git reset --hard HEAD`
5. Inspect the README file and note that everything is normal.
