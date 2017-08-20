# Simple example

	$ ./start > /dev/null 2>&1 &
	[1] 21003
	$ ./test
	Error! No key exists at: test/foo
	Success! Data written to: test/foo
	bar
	FOO=bar
	$ ./test
	bar
	Success! Data written to: test/foo
	bar
	FOO=bar
	$ ./simple_service
	Setup service and checks. Service check should be failing.
	Serving HTTP on 0.0.0.0 port 3000 (http://0.0.0.0:3000/) ...
	Started http.server. Service check should be passing.
	Stopped http.server. Check should failing.
	./simple_service: line 14: 21055 Terminated: 15          python -m http.server --cgi 3000
	Deregistered service and checks. Done.
