# gpu_cloud
How to set up a machine for ML in the cloud

[Tensor Dock](https://www.tensordock.com/)

- To avoid typing password, do in local terminal `ssh-copy-id -i ~/.ssh/id_ed25519.pub -p 10292 user@216.234.102.170`
  > - The `-p 10292 user@216.234.102.170` can be found on tensordock page
- `rsync -arlptP -e "ssh -p 10292" user@216.234.102.170:/home/user/workspace/ /home/bouteille/Documents/tensordock-rsync` will send to local all my files in the remote SSH (only send diff)
  > - Should be use from local server ! (for sending and receving from ssh)
   > - **For large files: https://serverfault.com/questions/1103253/how-to-have-rsync-split-files-into-smaller-bits-and-combine-them-upon-finishing**
   > - ask chatgpt the difference between `--append-verify` and  `--inplace`
