Stderr for source:  Volumes.md_working_2.dat   
Download: [zipped raw stdout](Volumes.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Volumes.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action INSPHERE with label sp : keyword DATA is compulsory for this action
[runnervm3jyl0:48414] *** Process received signal ***
[runnervm3jyl0:48414] Signal: Aborted (6)
[runnervm3jyl0:48414] Signal code:  (-6)
[runnervm3jyl0:48414] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd407a45330]
[runnervm3jyl0:48414] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd407a9eb2c]
[runnervm3jyl0:48414] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd407a4527e]
[runnervm3jyl0:48414] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd407a288ff]
[runnervm3jyl0:48414] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd407ea5ff5]
[runnervm3jyl0:48414] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd407ebb0da]
[runnervm3jyl0:48414] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd407ea5a55]
[runnervm3jyl0:48414] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd407ea5a6f]
[runnervm3jyl0:48414] [ 8] plumed(+0x13209)[0x557f5ce5c209]
[runnervm3jyl0:48414] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd407a2a1ca]
[runnervm3jyl0:48414] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd407a2a28b]
[runnervm3jyl0:48414] [11] plumed(+0x134a5)[0x557f5ce5c4a5]
[runnervm3jyl0:48414] *** End of error message ***
</pre>
{% endraw %}
