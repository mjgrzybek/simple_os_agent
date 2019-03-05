# simple_os_agent
OS agent using non-elevated user for gathering basic system info.
# usage
## any command
`ansible all -u gtg -e 'ansible_python_interpreter=/usr/bin/python3' -a "echo asd"`
## ping
`ansible all -u gtg -e 'ansible_python_interpreter=/usr/bin/python3' -m ping`
## system setup info
`ansible all -u gtg -e 'ansible_python_interpreter=/usr/bin/python3' -m setup`
