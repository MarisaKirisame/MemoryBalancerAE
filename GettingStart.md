The Getting Started Guide should contain setup instructions (including, for example, a pointer to the VM player software, its version, passwords if needed, etc.) and basic testing of your artifact that you expect a reviewer to be able to complete in 30 minutes. Reviewers will follow all the steps in the guide during an initial kick-the-tires phase. The Getting Started Guide should be as simple as possible, and yet it should stress the key elements of your artifact. Anyone who has followed the Getting Started Guide should have no technical difficulties with the rest of your artifact.

Install v8
https://v8.dev/docs/build
use hash xxx
apply diff yyy

Install chrome
https://www.chromium.org/developers/how-tos/get-the-code/
use has zzz
inside chrome there is also a v8, do the above v8 step for that v8 also
libdav1d seems to be diffcult to download, here is a copy of that - copy it in and gclient sync again if it fail on that

Install MemoryBalancer
the zip is in the repo
'make' and thats it

The three repo should be in the same directory.

login to websites:
python3 python/login.py
then ask me for the twitter/facebook/gmail login during kick the tires (I dont want to put it on web because there are crawlers).

additionally, it will be good to try out the jetstream and webi eval in StepByStep - they take <4 hours to run in total, and getting them running imply a high probability of the others running.
