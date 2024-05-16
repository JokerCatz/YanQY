# hint

    cat require.md
    
    git branch branch_a
    git checkout branch_a
    echo "a.md" > a.md
    git status
    git add a.md
    git status
    git commit -m "branch_a"
    git log
    
    git branch branch_b
    git checkout branch_b
    echo "b.md" > b.md
    git add b.md
    git commit -m "branch_b"
    
    git branch branch_c
    git checkout branch_c
    echo "c.md" > c.md
    git add c.md
    git commit -m "branch_c"
    
    git branch branch_d
    git checkout branch_d
    echo "d.md" > d.md
    git add d.md
    git commit -m "branch_d"
    
    git branch branch_e
    git checkout branch_e
    echo "e.md" > e.md
    git add e.md
    git commit -m "branch_e"
    
    git checkout branch_d
    git rebase branch_b -i // fix branch_c "pickup" to "drop"
    ls // no c.md
    
    git checkout branch_e
    ls // has c.md
    git rebase main -i // fix branch_c "pickup" to "drop"
    ls // no c.md