#Signature Creator

AppleScript (createSignature.scpt) program grabs information from a user which then uses a shell script (sig.sh) to place that information into an HTML document that is turned into a webarchive by webarchiver for use in Mail (or without webarchiver for Thunderbird). Designed as a starting point - from where it stands it needs to be customized for use but should serve as a half decent starting point.

More about how this was developed will be posted on http://chealion.ca (link will be added at a later date after I post it)

Big Thank You to Paul William's blog entry on [webarchiver: Create safari webarchives from the command line.](http://www.entropytheblog.com/blog/2008/11/webarchiver-create-safari-webarchives-from-the-command-line) The source code is available on: [GitHub](http://github.com/paulwilliam/webarchiver/tree/master)


##Build Steps:

1. Create webarchiver using XCode
2. Open up .scpt file and edit the file customizing information asked as required.
3. Open up .sh file and edit the file to use customized information.
4. Create a new application using Script Editor using the .scpt file
5. Copy the built webarchiver executable and sig.sh into the Resources folder of the new application.

------------------

##Caveats and Limitations

1. Uses ~/sigtmp instead of /tmp because in testing with network based user directories /tmp wouldn't always permit write access. No idea why that was but ~/sigtmp only appears during the script.
2. Only creates the signature - does not apply the signature in Thunderbird or Mail. When this was developed (10.5.4) the AppleScript dictionary for Mail was broken when dealing with Signatures. (Among many other AppleScript issues with Mail in Leopard)
3. Assumes only one Thunderbird profile - if you have multiples it only picks the first one alphanumerically.

-------------------

## Submodules Used:

Webarchiver.git (Applescripts/Signatures) - [GitHub : paulwilliam : webarchiver](http://github.com/paulwilliam/webarchiver/tree/master)

-------------------

The MIT License

Copyright (c) 2009 Micheal Jones

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE