Stderr for source:  work/plumed_ex4.dat   
Download: [zipped raw stdout](plumed_ex4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action HISTOGRAM with label @s16 : set NORMALIZATION=true/false when using LOGWEIGHTS as otherwise the weights are ignored. Alternatively, learn to use the new syntax for histograms with KDE/ACCUMULATE to have more control over what PLUMED is calculating
[runnervm3jyl0:81123] *** Process received signal ***
[runnervm3jyl0:81123] Signal: Aborted (6)
[runnervm3jyl0:81123] Signal code:  (-6)
[runnervm3jyl0:81123] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9f18645330]
[runnervm3jyl0:81123] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9f1869eb2c]
[runnervm3jyl0:81123] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9f1864527e]
[runnervm3jyl0:81123] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9f186288ff]
[runnervm3jyl0:81123] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9f18aa5ff5]
[runnervm3jyl0:81123] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9f18abb0da]
[runnervm3jyl0:81123] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9f18aa5a55]
[runnervm3jyl0:81123] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9f18aa5a6f]
[runnervm3jyl0:81123] [ 8] plumed_master(+0x146dd)[0x56148eb256dd]
[runnervm3jyl0:81123] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9f1862a1ca]
[runnervm3jyl0:81123] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9f1862a28b]
[runnervm3jyl0:81123] [11] plumed_master(+0x15365)[0x56148eb26365]
[runnervm3jyl0:81123] *** End of error message ***
</pre>
{% endraw %}
