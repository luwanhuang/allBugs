all button, for check or for login, should add block to prevent user click multiple times.
```
const [block, setBlock] = useState(false)
```
```
<input
                        className={"submit"}
                        disabled={block}
                        type='button'
                        value={"Check In"}
                        onClick={() => {
                            setBlock(true)
                            summit()
                        }}
                    ></input>
```
