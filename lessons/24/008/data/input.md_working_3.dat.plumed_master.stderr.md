Stderr for source:  input.md_working_3.dat   
Download: [zipped raw stdout](input.md_working_3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](input.md_working_3.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::Exception'
what():
Action "MAZE_OPT_ANNEALING" is not known.
[fv-az1279-640:05812] *** Process received signal ***
[fv-az1279-640:05812] Signal: Aborted (6)
[fv-az1279-640:05812] Signal code:  (-6)
[fv-az1279-640:05812] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7facfa045330]
[fv-az1279-640:05812] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7facfa09eb2c]
[fv-az1279-640:05812] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7facfa04527e]
[fv-az1279-640:05812] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7facfa0288ff]
[fv-az1279-640:05812] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7facfa4a5ff5]
[fv-az1279-640:05812] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7facfa4bb0da]
[fv-az1279-640:05812] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7facfa4a5a55]
[fv-az1279-640:05812] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7facfa4a5a6f]
[fv-az1279-640:05812] [ 8] plumed_master(+0x146dd)[0x5630184466dd]
[fv-az1279-640:05812] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7facfa02a1ca]
[fv-az1279-640:05812] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7facfa02a28b]
[fv-az1279-640:05812] [11] plumed_master(+0x15365)[0x563018447365]
[fv-az1279-640:05812] *** End of error message ***
</pre>
{% endraw %}
