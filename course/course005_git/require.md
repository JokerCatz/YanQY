# require : git ignore files and fix ignored file as default config

1. add a `config.ini` file , file body is `a..e` one line one char , as first commit
2. add `.gitignore` to ignore `config.ini` , as second commit
3. fix `config.ini` , `c` as `Z` , and force add fixed file to commit , and last commit , and send PR