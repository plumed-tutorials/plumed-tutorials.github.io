Stderr for source:  work/plumed_ex3.dat   
Download: [zipped raw stdout](plumed_ex3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action LANDMARK_SELECT_FPS with label fps : input analysis action was not specified use USE_OUTPUT_DATA_FROM
[fv-az1690-151:06473] *** Process received signal ***
[fv-az1690-151:06473] Signal: Aborted (6)
[fv-az1690-151:06473] Signal code:  (-6)
[fv-az1690-151:06473] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1ee7c45330]
[fv-az1690-151:06473] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1ee7c9eb2c]
[fv-az1690-151:06473] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1ee7c4527e]
[fv-az1690-151:06473] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1ee7c288ff]
[fv-az1690-151:06473] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1ee80a5ff5]
[fv-az1690-151:06473] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1ee80bb0da]
[fv-az1690-151:06473] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1ee80a5a55]
[fv-az1690-151:06473] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1ee80a5a6f]
[fv-az1690-151:06473] [ 8] plumed(+0x13209)[0x5646ade5b209]
[fv-az1690-151:06473] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1ee7c2a1ca]
[fv-az1690-151:06473] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1ee7c2a28b]
[fv-az1690-151:06473] [11] plumed(+0x134a5)[0x5646ade5b4a5]
[fv-az1690-151:06473] *** End of error message ***
</pre>
{% endraw %}
