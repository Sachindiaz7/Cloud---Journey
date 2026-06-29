#Day 2 - Processes and Pipe Operator

ps                    - show current session processes
ps aux                - show ALL processes on system
ps aux | grep bash    - filter processes by name
top                   - live process monitor (press q to quit)
kill PID              - terminate a process by PID number
sleep 500 &           - run process in background
&                     - run any command in background


#Pipe Operator
|                     - sends output of the one command into another
wc-l                  - count number of lines


#Real Examples
ps aux | grep python  - check if python app running 
ls "/mnt/c/JUST CHILL/MOVIES/TAMIL" -1 | wc -l     - counted 19 Tamil movies!!
