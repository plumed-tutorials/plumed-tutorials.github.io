Stderr for source:  histograms.md_working_9.dat   
Download: [zipped raw stdout](histograms.md_working_9.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_9.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCES with label d1 : keyword ATOMS could not be read correctly
[fv-az1755-505:07976] *** Process received signal ***
[fv-az1755-505:07976] Signal: Aborted (6)
[fv-az1755-505:07976] Signal code:  (-6)
[fv-az1755-505:07976] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5e83045330]
[fv-az1755-505:07976] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f5e8309eb2c]
[fv-az1755-505:07976] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f5e8304527e]
[fv-az1755-505:07976] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f5e830288ff]
[fv-az1755-505:07976] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f5e834a5ff5]
[fv-az1755-505:07976] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f5e834bb0da]
[fv-az1755-505:07976] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f5e834a5a55]
[fv-az1755-505:07976] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f5e834a5a6f]
[fv-az1755-505:07976] [ 8] plumed(+0x13209)[0x55f0fdd80209]
[fv-az1755-505:07976] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f5e8302a1ca]
[fv-az1755-505:07976] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f5e8302a28b]
[fv-az1755-505:07976] [11] plumed(+0x134a5)[0x55f0fdd804a5]
[fv-az1755-505:07976] *** End of error message ***
</pre>
{% endraw %}
