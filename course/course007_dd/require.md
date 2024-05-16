# require backup

1. here show how to easy way to backup and compression linux disk (recommand `/dev/sda` only 8GB- , and change `/dev/sda` to your device location)
1. `dd if=/dev/zero of=./zero.img && rm ./zero.img` , this command can fill all useless disk to zero for best compression.
1. `dd if=/dev/sda | gzip > ~/dd_dev_sda_20241118.gz` , backup full disk to single dd file
1. create a file `answer.md` . show me how to rollback the dd image to the disk
1. and show me how to only backup `/dev/sda1`
1. and show me how to mount a dd file (without compression will be more easy)
