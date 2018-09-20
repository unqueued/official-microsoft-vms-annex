Quick and dirty URL extraction:
awk '{print $1}' < windows-vms | grep https

git annex addurl --relaxed --raw --pathdepth=-1

oh wait, --fast is what I wanted...

https://git-annex.branchable.com/git-annex-addurl/

git annex addurl --pathdepth=-1 --fast --batch

awk '{print $1}' < windows-vms | grep https > URLS.txt

