# require

1. new 5 branch call `branch_a..branch_e` , per branch add new file and file body same as file name , like `a.md .. e.md` , inheritance last branch (so last branch has all files)
1. `branch_d` git rebase to `branch_b` , and remember the `branch_e` need rebase to last `branch_d` (for remove the `branch_c` at inheritance list)
1. PR the `branch_e`
