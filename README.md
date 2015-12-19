# hh_git_3

git update-index --add task3.txt

git write-tree // 505d68cadeecc923ad6884212120ac3dabb4329e

echo "commit Kapiton42 1" | git commit-tree 505d68cadeecc923ad6884212120ac3dabb4329e // 791f3e695896f25f68d40335205e0685ab677fa5


git update-index task3.txt

git update-index --add task3_new.txt

git write-tree // f39f521efd092454fb65b2d559183c545773e4e2

echo "commit Kapiton42 1" | git commit-tree f39f521efd092454fb65b2d559183c545773e4e2 -p 791f3e695896f25f68d40335205e0685ab677fa5 // c28580f5038c67bfbf1d912985a2a2930424c072


git read-tree --prefix=gittask 505d68cadeecc923ad6884212120ac3dabb4329e

git write-tree // 19a09706188cab3801e4f8704366ceb36a3f941b

echo "commit Kapiton42 3" | git commit-tree 19a09706188cab3801e4f8704366ceb36a3f941b -p c28580f5038c67bfbf1d912985a2a2930424c072 // 7a675e1bd11a4261bb7a80a62a3d7bc61d6eec4c


echo "7a675e1bd11a4261bb7a80a62a3d7bc61d6eec4c" > ./.git/refs/heads/master
