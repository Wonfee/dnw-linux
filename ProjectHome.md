# Introduction #
> This tool can be used to download image file to s3c24xx or s2c64xx based board fastly.

> If you are looking for **the newest Linux kernel for ok6410**, please goto: http://code.google.com/p/linux-ok6410

(This project is based on the code from internet)

# Download source #
Goto [download](http://code.google.com/p/dnw-linux/downloads/list) page to get source tarball.


or clone source from https://github.com/changbindu/dnw-linux.git via git:
```
   $ git clone https://github.com/changbindu/dnw-linux.git
```

# How to #
(1) build and install
```
   $ cd dnw-linux
   $ sudo make install
```

(2) tool usage
> Connect board to PC and open minicom. Boot board and enter U-Boot command line mode. Then run command "dnw <download address>" in U-Boot. U-Boot may print bellow message:
> Insert a OTG cable into the connector! <br>
<blockquote>OTG cable Connected! <br>
Now, Waiting for DNW to transmit data <br></blockquote>

<blockquote>Now, you can download your file to board by follow command on PC end:<br>
<pre><code>    $ sudo dnw [file_to_download]<br>
</code></pre>
The downloading speed tested is about 3.8M/S.</blockquote>

Notes:<br>
<ul><li>Above steps have only downloaded file to board's RAM, so you need  flash it to nand via U-Boot command "nand write" .</li></ul>

<blockquote>If above doesn't work, pls check if you can see bellow message in <code>dmesg</code>.<br>
</blockquote><blockquote>usb 1-1: new full speed USB device using uhci_hcd and address 2 <br>
usb 1-1: configuration #1 chosen from 1 choice <br>
secbulk:secbulk probing... <br>
secbulk:bulk out endpoint found! <br></blockquote>

For details see <a href='https://raw.github.com/changbindu/dnw-linux/master/README'>README</a>.<br>
<br>
Best Regards<br>
<table><thead><th>Du, Changbin < changbin.du@gmail.com ></th></thead><tbody></tbody></table>

Links:<br>
<a href='http://code.google.com/p/linux-ok6410'>Linux kernel for ok6410 board</a>