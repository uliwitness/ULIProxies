What is it
----------

A few helper classes that can be used as proxies for other objects.
This usually involves some sort of threading or time-delay of messages.


What is what
------------

UKMainThreadProxy - Use this on an object to send a message on one threading
and have it automatically packaged up and sent on the main thread. This is
useful for cases for messages that take more than 2 or non-object parameters.

UKPushbackMessenger - This object coalesces a message sent to it transparently
(It does not look at message parameters, only the method name). And sends it
if no additional identical message comes in after a specified delay. This is
useful to e.g. perform a slightly expensive operation as soon as the user
pauses in typing, but not on every character.

UKThreadMessenger - Executes all messages it is sent on a dedicated thread.
This is bad, old, busted code. Use NSOperationQueue and blocks instead.


License
-------

	Copyright 2004-2014 by Uli Kusterer.
	
	This software is provided 'as-is', without any express or implied
	warranty. In no event will the authors be held liable for any damages
	arising from the use of this software.
	
	Permission is granted to anyone to use this software for any purpose,
	including commercial applications, and to alter it and redistribute it
	freely, subject to the following restrictions:
	
	   1. The origin of this software must not be misrepresented; you must not
	   claim that you wrote the original software. If you use this software
	   in a product, an acknowledgment in the product documentation would be
	   appreciated but is not required.
	
	   2. Altered source versions must be plainly marked as such, and must not be
	   misrepresented as being the original software.
	
	   3. This notice may not be removed or altered from any source
	   distribution.
