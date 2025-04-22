Stderr for source:  input.md_working_2.dat   
Download: [zipped raw stdout](input.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](input.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::Exception'
what():
Action "MAZE_OPT_ANNEALING" is not known.
[fv-az1279-640:05765] *** Process received signal ***
[fv-az1279-640:05765] Signal: Aborted (6)
[fv-az1279-640:05765] Signal code:  (-6)
[fv-az1279-640:05765] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f15c8045330]
[fv-az1279-640:05765] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f15c809eb2c]
[fv-az1279-640:05765] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f15c804527e]
[fv-az1279-640:05765] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f15c80288ff]
[fv-az1279-640:05765] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f15c84a5ff5]
[fv-az1279-640:05765] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f15c84bb0da]
[fv-az1279-640:05765] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f15c84a5a55]
[fv-az1279-640:05765] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f15c84a5a6f]
[fv-az1279-640:05765] [ 8] plumed_master(+0x146dd)[0x557742ce36dd]
[fv-az1279-640:05765] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f15c802a1ca]
[fv-az1279-640:05765] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f15c802a28b]
[fv-az1279-640:05765] [11] plumed_master(+0x15365)[0x557742ce4365]
[fv-az1279-640:05765] *** End of error message ***
</pre>
{% endraw %}
