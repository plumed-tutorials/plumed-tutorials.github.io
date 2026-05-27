Stderr for source:  Steinhardt.md_working_16.dat   
Download: [zipped raw stdout](Steinhardt.md_working_16.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_16.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[runnervmg397c:79995] *** Process received signal ***
[runnervmg397c:79995] Signal: Aborted (6)
[runnervmg397c:79995] Signal code:  (-6)
[runnervmg397c:79995] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd100a45330]
[runnervmg397c:79995] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd100a9eb2c]
[runnervmg397c:79995] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd100a4527e]
[runnervmg397c:79995] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd100a288ff]
[runnervmg397c:79995] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd100ea5ff5]
[runnervmg397c:79995] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd100ebb0da]
[runnervmg397c:79995] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd100ea5a55]
[runnervmg397c:79995] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd100ea5a6f]
[runnervmg397c:79995] [ 8] plumed(+0x13209)[0x56024a894209]
[runnervmg397c:79995] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd100a2a1ca]
[runnervmg397c:79995] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd100a2a28b]
[runnervmg397c:79995] [11] plumed(+0x134a5)[0x56024a8944a5]
[runnervmg397c:79995] *** End of error message ***
</pre>
{% endraw %}
