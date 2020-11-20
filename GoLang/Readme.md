after install Golang in new computer, even I already set Env variable, still can not check go version <br/>
googled and find just input <br/>
$env:Path = [System.Environment]::GetEnvironmentVariable("Path","Machine")  <br/>
it works! <br/>
this command looks like get env variable from system.environment, but do not know why it work right now, so mark this until I know how it works.
