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
[runnervm3jyl0:47823] *** Process received signal ***
[runnervm3jyl0:47823] Signal: Aborted (6)
[runnervm3jyl0:47823] Signal code:  (-6)
[runnervm3jyl0:47823] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4736045330]
[runnervm3jyl0:47823] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f473609eb2c]
[runnervm3jyl0:47823] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f473604527e]
[runnervm3jyl0:47823] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f47360288ff]
[runnervm3jyl0:47823] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f47364a5ff5]
[runnervm3jyl0:47823] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f47364bb0da]
[runnervm3jyl0:47823] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f47364a5a55]
[runnervm3jyl0:47823] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f47364a5a6f]
[runnervm3jyl0:47823] [ 8] plumed(+0x13209)[0x55a981b4e209]
[runnervm3jyl0:47823] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f473602a1ca]
[runnervm3jyl0:47823] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f473602a28b]
[runnervm3jyl0:47823] [11] plumed(+0x134a5)[0x55a981b4e4a5]
[runnervm3jyl0:47823] *** End of error message ***
</pre>
{% endraw %}
