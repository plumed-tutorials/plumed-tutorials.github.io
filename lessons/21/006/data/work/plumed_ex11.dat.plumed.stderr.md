Stderr for source:  work/plumed_ex11.dat   
Download: [zipped raw stdout](plumed_ex11.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex11.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: MORE_THAN LABEL=fcub ARG=cub SWITCH=SMAP R_0=0.45 D_0=0.0 A=8 B=8
Maybe a missing space or a typo?
[runnervm3jyl0:48021] *** Process received signal ***
[runnervm3jyl0:48021] Signal: Aborted (6)
[runnervm3jyl0:48021] Signal code:  (-6)
[runnervm3jyl0:48021] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff779445330]
[runnervm3jyl0:48021] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff77949eb2c]
[runnervm3jyl0:48021] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff77944527e]
[runnervm3jyl0:48021] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff7794288ff]
[runnervm3jyl0:48021] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff7798a5ff5]
[runnervm3jyl0:48021] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff7798bb0da]
[runnervm3jyl0:48021] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff7798a5a55]
[runnervm3jyl0:48021] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff7798a5a6f]
[runnervm3jyl0:48021] [ 8] plumed(+0x13209)[0x55c97884d209]
[runnervm3jyl0:48021] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff77942a1ca]
[runnervm3jyl0:48021] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff77942a28b]
[runnervm3jyl0:48021] [11] plumed(+0x134a5)[0x55c97884d4a5]
[runnervm3jyl0:48021] *** End of error message ***
</pre>
{% endraw %}
