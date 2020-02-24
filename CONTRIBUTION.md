# Contribution

Please read the following steps first before you contribute.

1. Fork this repository first

```
git clone git@github.com:ZattWine/mm-phone-numbering.git
```

2. Create a new branch and checkout
```
$ git branch your-new-branch-name
$ git checkout your-new-branch-name
```
or
```
$ git checkout -b my-new-branch-name
```
After you finished these steps, you are able to contribute.

Each operator has the following structure in my `data.json`

```json
{
        "operator": "Mpt",
        "numbers": [
            {
                "area_code": 9,
                "start_number": "884 xxx - xxx",
                "digit_length": 10,
                "system_type": "WCDMA / GSM",
                "digit_length_description": "Digit Length includes Area Code.",
                "operator": "Mpt",
                "remark": ""
            },
            {
                "area_code": 9,
                "start_number": "885 xxx - xxx",
                "digit_length": 10,
                "system_type": "WCDMA / GSM",
                "digit_length_description": "Digit Length includes Area Code.",
                "operator": "Mpt",
                "remark": ""
            }
        ]
}
```

You can add new phone number format below the last item within `numbers` array.

```json
{
   "area_code": 9,
   "start_number": "your number format (eg: xxx xxx - xxx)",
   "digit_length": 10,
   "system_type": "type (eg. GSM | WCDMA / GSM)",
   "digit_length_description": "Digit Length includes Area Code.",
   "operator": "Mpt | Telenor | MyTel | Ooredoo | MecTel | Other",
   "remark": ""
}
```

If you want to add a new operator, you can add data as follow.

```json
[
    // other operators
    ,
    {
    	"operator" : "operator name",
    	"numbers" : [
    		"area_code" : Number,
    		"start_number" : String,
    		"digit_length" : Number,
    		"system_type" : String,
    		"digit_length_description" : String,
    		"operator" : String,
    		"remark" : String,
		]
    }
]
```

If you have completed, push to the branch.

```
$ git add .
$ git commit -m "your commit"
$ git push -u origin your-new-branch-name
```

And then, submit a `pull request` against the `your-new-branch-name` branch.

