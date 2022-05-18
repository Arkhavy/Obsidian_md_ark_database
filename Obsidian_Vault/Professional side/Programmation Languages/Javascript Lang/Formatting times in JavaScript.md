#Javascript 

Format times with `Intl.DateTimeFormat()` constructor

```JavaScript
const todayDate = new Date()

const shortFormat = new Intl.DateTimeFormat('en-US', { timeStyle: 'long' })

console.log(shortFormat.format(todayDate))
// 8:27 AM

const longFormat = new Intl.DateTimeFormat('en-US', { timeStyle: 'long' })

console.log(longFormat.format(todayDate))
// 8:27:20 AM GMT+2
```

```JavaScript
const todayDate = new Date()

const formatDate = new Intl.DateTimeFormat('en-US', {
	hour: "numeric",
	minute: "2-digit",
	second: "2-digit",
	timeZone: "CET",
	timeZoneName: "short",
})

const formatted = formatDate.format(todayDate)

console.log(formatted)
// 8:32:37 AM GMT+02:00
```