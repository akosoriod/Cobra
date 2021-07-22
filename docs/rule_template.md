# Rule Template
```xml
<?xml version="1.0" encoding="UTF-8"? >

<cobra document="https://github.com/WhaleShark-Team/cobra">
    <name value="HardcodedToken/Key"/>
    <language value="*"/>
    <match mode="regex-only-match"><! [CDATA[(?! [\d]{32})(?! [a-fA-F]{32})([a-f\d]{32}|[A-F\d]{32})]]></match>
    <level value="2"/>
    <test
        <case assert="true" remark="sha1"><! [CDATA["41a6bc4d9a033e1627f448f0b9593f9316d071c1"]></case
        <case assert="true" remark="md5 lower"><! [CDATA["d042343e49e40f16cb61bd203b0ce756"]]></case>
        <case assert="true" remark="md5 upper"><! [CDATA[C787AFE9D9E86A6A6C78ACE99CA778EE]]></case>
        <case assert="false"><! [CDATA[please like and subscribe to my]]></case>
        <case assert="false"><! [CDATA[A32efC32c79823a2123AA8cbDDd3231c]]></case>
        <case assert="false"><! 
        <case assert="false"><! [CDATA[01110101001110011101011010101001]]></case>
        <case assert="false"><! [CDATA[0000000000000000000000000000000000]]></case>
    </test>
    <solution
        ## Security risks
        Hard-coded passwords

        ## Fix solution
        Pull out the passwords and put them uniformly in the config file, the config file is not in git
    </solution>
    <status value="on"/>
    <author name="Feei" email="feei@feei.cn"/>
</cobra>
```


## Rule field specification

|Field (English)|Field (Chinese)|Required|Type|Description|Example|
|--|--|--|--|--|--|--|--|--|
|`name`|Rule name|Yes|`string`|Description|Rule name|`<name value="Logger sensitive information" />`|
|`language`|Rule language|is|`string`|set the development language the rule targets, see `languages`|`<language value="php" />`|
|`match`|match rule1|yes|`string`|match rule1|`<match mode="regex-only-match"><! [CDATA[regex content]]></match>`|
|`match2`|match rule 2|no||`string`|match rule 2|`<match2 block="in-function-up"><! [CDATA[regex content]]></match2>`|
|`repair`|fix rule|no|`string`|matches to this rule, then it doesn't count as a vulnerability|`<repair block=""><! [CDATA[regex content]]></repair>`|
|`level`|impact level|is|`integer`|to mark the level of vulnerability hazard swept by the rule, using numbers 1-10.|`<level value="3" />`|
|`solution`|fix solution|is|`string`|the **security risk** and **fix solution** corresponding to the vulnerabilities scanned by this rule|`<solution>detailed security risk and fix solution</solution>`|
|`test`|test case|is|`case`|the test case corresponding to this rule|`<test><case assert="true"><! [CDATA[test for vulnerable code]]></case><case assert="false"><! [CDATA[test for code that is not vulnerable]]></case></test>`|
|`status`|whether to turn on|yes|`boolean`|whether to turn on scanning for this rule, using `on`/`off` to mark|`<status value="1" />`|
|`author`|the rule author|yes|`attr`|the rule author's name and email|`<author name="Feei" email="feei@feei.cn" />`|

## Core field `<match>`/`<match2>`/`<repair>` writing specification

#### `<match>` Mode (rule mode for `<match>`)
> Used to describe the rule type, which can only be used in `<match>`.

|Mode|type|default mode|support language|description|
|--|--|--|--|--|--|
|regex-only-match|regular-only-match|is|yes|*| defaults to this mode, but needs to be explicitly written in the rules file. Match as a regular, and a match to content counts as a vulnerability|
|regex-param-controllable|regular-param-controllable|no|PHP/Java|matches in regular mode, matching a variable that is externally controllable is a vulnerability|
|function-param-controllable|function-param-controllable|no|PHP|Write the function name, will search for all calls to the function, if the parameter can be controlled externally then it is a vulnerability. |find-extension
|find-extension|Find the specified suffix file|No|*|Finding the specified suffix file counts as a vulnerability|

#### `<match2>`/`<repair>` Block (the match block for `<match2>`/`<repair>`)
> Used to describe the location of the block of code to be matched, and can only be used in `<match2>` or `<repair>`.

|block|description|
|--|--|
| in-current-line | The line triggered by the first rule |
| in-function | within the function triggered by the first rule |
| in-function-up | above the line triggered by the first rule, within the function body |
| in-function-down | below the line triggered by the first rule, inside the function body |
| in-file | inside the file triggered by the first rule
| in-file-up | above the line triggered by the first rule, inside the file |
| in-file-down | below the line triggered by the first rule, within the file |

---
Next Chapter: [Sample Rule](http://cobra.feei.cn/rule_demo)


Translated with www.DeepL.com/Translator (free version)