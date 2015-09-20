# kronos
It'll be a natural language to crontab syntax parser. **[But for now, move on](http://tom.preston-werner.com/2010/08/23/readme-driven-development.html).**

## Quickstart

Kronos translates natural English sentences, such as "everyday at 5pm" to crontab syntax `* 17 * * *`
`(kronos "every thursday and friday at midnight")` would return a string `"* 0 * * 4,5"`.

## License

See [LICENSE](LICENSE)
