cd Bootimgutils
./split_bootimg.pl boot.img
mkdir ramdisk
cd ramdisk
gzip -dc ../boot.img-ramdisk.gz | cpio -i
cd ..

--------

./repack_bootimg.pl boot.img-kernel ramdisk bootnew.img
