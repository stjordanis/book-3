---
layout: content
title: NuShell Map To Other Languages
prev: Coming from Bash
next: NuShell Operator Map
link_prev: /en/coming_from_bash.html
link_next: /en/nushell_operator_map.html
---

The idea behind this table is to help you understand how NuShell built-ins and plug-ins relate to other known languages. We've tried to produce a map of all the nushell commands and what their equivalents are in other languages. Contributions are welcome.

Note: this table assumes Nushell 0.13.1 or later.


| NuShell                | SQL                           | .Net LINQ (C#)                                       | PowerShell (without external modules)      | Bash                                            |
| ---------------------- | ----------------------------- | ---------------------------------------------------- | ------------------------------------------ | ----------------------------------------------- |
| alias                  | N/A                           | N/A                                                  | alias                                      | alias                                           |
| append                 | N/A                           | N/A                                                  | -Append                                    |                                                 |
| args                   | N/A                           | N/A                                                  |                                            |                                                 |
| autoview               | N/A                           | N/A                                                  |                                            |                                                 |
| average(`*`)           | avg                           | Average()                                            | Measure-Object, measure                    |                                                 |
| binaryview(`*`)        | N/A                           |                                                      | Format-Hex                                 |                                                 |
| calc, = math         | math operators                | Aggregate, Average, Count, Max, Min, Sum             |                                            | bc                                              |
| cd                     | N/A                           | N/A                                                  | Set-Location, cd                           | cd                                              |
| clear                  | N/A                           | N/A                                                  | Clear-Host                                 | clear                                           |
| clip                   | N/A                           | N/A                                                  | Set-Clipboard, scb                         | clip, clipboard, xclip, pbcopy                  |
| compact                |                                |                                                      |                                            |                                                 |
| config                 | N/A                           | N/A                                                  | $Profile                                   | vi .bashrc, .profile                            |
| count                  | count                         | Count                                                | Measure-Object, measure                    |                                                 |
| cp                     | N/A                           | N/A                                                  | Copy-Item, cp, copy                        | cp                                              |
| date                   | NOW() / getdate()             | DateTime class                                       | Get-Date                                   | date                                            |
| debug                  |                               |                                                      |                                            |                                                 |
| default                |                               |                                                      |                                            |                                                 |
| drop                   |                               |                                                      |                                            |                                                 |
| du                     | N/A                           | N/A                                                  |                                            | du                                              |
| each                   | cursor                        |                                                      | ForEach-Object, foreach, for               |                                                 |
| echo                   | print                         | N/A                                                  | Write-Output, write                        | echo                                            |
| edit renamed to update | As                            | N/A                                                  |                                            |                                                 |
| enter                  | N/A                           | N/A                                                  |                                            |                                                 |
| evaluate_by            |                               |                                                      |                                            |                                                 |
| exit                   | N/A                           |                                                      | exit                                       | exit                                            |
| fetch(`*`)             | N/A                           | HttpClient,WebClient, HttpWebRequest/Response        | Invoke-WebRequest                          | wget                                            |
| first                  | top, limit                    | First, FirstOrDefault                                | Select-Object -First                       | head                                            |
| format                 |                               | String.Format()                                      | String.Format()                            |                                                 |
| from bson              | N/A                           | N/A                                                  | N/A                                        |                                                 |
| from csv               | import flatfile               | N/A                                                  | Import-Csv, ConvertFrom-Csv                |                                                 |
| from eml               | N/A                           | N/A                                                  | N/A                                        |                                                 |
| from ics               | N/A                           | N/A                                                  | N/A                                        |                                                 |
| from ini               | N/A                           | N/A                                                  | N/A                                        |                                                 |
| from json              | openjson                      | N/A                                                  | ConvertFrom-Json                           |                                                 |
| from ods               | N/A                           | N/A                                                  | N/A                                        |                                                 |
| from sqlite            | N/A                           | N/A                                                  | N/A                                        |                                                 |
| from ssv               | import flatfile               | N/A                                                  | N/A                                        |                                                 |
| from toml              | N/A                           | N/A                                                  | N/A                                        |                                                 |
| from tsv               | import flatfile               | N/A                                                  | N/A                                        |                                                 |
| from url               | N/A                           | N/A                                                  | N/A                                        |                                                 |
| from vcf               | N/A                           | N/A                                                  | N/A                                        |                                                 |
| from xlsx              | import                        | N/A                                                  | N/A                                        |                                                 |
| from xml               | cast(variable as xml)         | N/A                                                  | ConvertFrom-Xml                            |                                                 |
| from yaml              | N/A                           | N/A                                                  | N/A                                        |                                                 |
| get                    |                               | Select                                               | (cmd).column                               |                                                 |
| group_by               | group by                      | GroupBy, group                                       | Group-Object, group                        |                                                 |
| headers                |                               |                                                      |                                            |                                                 |
| help                   | sp_help                       | N/A                                                  | Get-Help, help, man                        | man                                             |
| histogram              | N/A                           | N/A                                                  |                                            |                                                 |
| history                | N/A                           | N/A                                                  | Get-History, history                       | history                                         |
| inc(`*`)               | N/A                           |                                                      | N/A                                        | N/A                                             |
| insert                 |                               |                                                      | Add-Member                                 |                                                 |
| is_empty               | is null                       | String.InNullOrEmpty()                               | String.InNullOrEmpty()                     |                                                 |
| keep                   | top,limit                     | Take                                                 | Select-Object -First                       | head                                            |
| keep_until             |                               |                                                      |                                            |                                                 |
| keep_while             |                               | TakeWhile                                            |                                            |                                                 |
| kill                   | N/A                           | N/A                                                  | Stop-Process, kill                         | kill                                            |
| last                   |                               | Last, LastOrDefault                                  | Select-Object -Last                        | tail                                            |
| lines                  | N/A                           | N/A                                                  | File.ReadAllLines()                        |                                                 |
| ls                     | N/A                           | N/A                                                  | Get-ChildItem, dir, ls                     | ls                                              |
| map_max_by             |                               |                                                      |                                            |                                                 |
| match(`*`)             | case when                     | RegEx                                                | [regex]                                    |                                                 |
| merge                  |                               |                                                      |                                            |                                                 |
| mkdir                  | N/A                           | N/A                                                  | mkdir, md                                  | mkdir                                           |
| mv                     | N/A                           | N/A                                                  | Move-Item, mv, move, mi                    | mv                                              |
| next                   |                               |                                                      |                                            |                                                 |
| nth                    | limit x offset y, rownumber = | ElemantAt(x)                                         | [x], indexing operator, ElementAt(x)       |                                                 |
| open                   |                               |                                                      | Get-Content, gc, cat, type                 | cat                                             |
| parse                  |                               |                                                      |                                            |                                                 |
| pick renamed to select | select                        | Select                                               | Select-Object, select                      |                                                 |
| pivot                  | pivot                         | N/A                                                  |                                            |                                                 |
| post(`*`)              | N/A                           | HttpClient,WebClient, HttpWebRequest/Response        | Invoke-WebRequest                          |                                                 |
| prepend                |                               |                                                      |                                            |                                                 |
| prev                   |                               |                                                      |                                            |                                                 |
| ps(`*`)                | N/A                           | N/A                                                  | Get-Process, ps, gps                       | ps                                              |
| pwd                    | N/A                           | N/A                                                  | Get-Location, pwd                          | pwd                                             |
| range                  |                               | Range                                                | 1..10, 'a'..'f'                            |                                                 |
| reduce_by              |                               |                                                      |                                            |                                                 |
| reject                 |                               |                                                      |                                            |                                                 |
| rename                 | N/A                           | N/A                                                  | Rename-Item, ren, rni                      | mv?                                             |
| reverse                |                               | Reverse                                              | [Array]::Reverse($var)                     |                                                 |
| rm                     | N/A                           | N/A                                                  | Remove-Item, del, erase, rd, ri, rm, rmdir | rm                                              |
| save                   | N/A                           | N/A                                                  | Write-Output, Out-File                     | > foo.txt                                       |
| shells                 | N/A                           | N/A                                                  | N/A                                        |                                                 |
| shuffle                |                               | Random                                               | $var                                       | Sort-Object {Get-Random}                        |
| size                   |                               |                                                      | Measure-Object, measure                    | wc                                              |
| skip                   | where row_number()            | Skip                                                 | Select-Object -Skip                        |                                                 |
| skip_until             |                               |                                                      |                                            |                                                 |
| skip_while             |                               | SkipWhile                                            |                                            |                                                 |
| sort_by                | order by                      | OrderBy, OrderByDescending, ThenBy, ThenByDescending | Sort-Object, sort                          |                                                 |
| split_by               |                               | String.Split()                                       | String.Split()                             |                                                 |
| split_column           |                               | N/A                                                  |                                            |                                                 |
| split_row              |                               | N/A                                                  |                                            |                                                 |
| str(`*`)               | string functions              | String class                                         | String class                               |                                                 |
| sum                    | sum                           | Sum()                                                | Measure-Object, measure                    |                                                 |
| sys(`*`)               | N/A                           | N/A                                                  | Get-ComputerInfo                           | uname, lshw, lsblk, lscpu, lsusb, hdparam, free |
| t_sort_by              |                               |                                                      |                                            |                                                 |
| table                  |                               |                                                      | Format-Table, ft, Format-List, fl          |                                                 |
| tags                   | N/A                           | N/A                                                  | N/A                                        |                                                 |
| textview(`*`)          | N/A                           | N/A                                                  | Get-Content, cat                           |                                                 |
| tree(`*`)              | N/A                           | N/A                                                  | tree                                       |                                                 |
| to bson                | N/A                           | N/A                                                  | N/A                                        |                                                 |
| to csv                 | N/A                           | N/A                                                  | Export-Csv, ConvertTo-Csv                  |                                                 |
| to html                | N/A                           | N/A                                                  | ConvertTo-Html                             |                                                 |
| to json                | N/A                           | N/A                                                  | ConvertTo-Json                             |                                                 |
| to md                  | N/A                           | N/A                                                  | N/A                                        |                                                 |
| to sqlite              | N/A                           | N/A                                                  | N/A                                        |                                                 |
| to toml                | N/A                           | N/A                                                  | N/A                                        |                                                 |
| to tsv                 | N/A                           | N/A                                                  | N/A                                        |                                                 |
| to url                 | N/A                           | N/A                                                  | N/A                                        |                                                 |
| to yaml                | N/A                           | N/A                                                  | N/A                                        |                                                 |
| touch                  | N/A                           | N/A                                                  | Set-Content                                | touch                                           |
| trim                   | rtrim,ltrim                   | String.Trim()                                        | String.Trim()                              |                                                 |
| uniq                   | distinct                      | Distinct                                             | Get-Unique, gu                             | uniq                                            |
| version                | select @@version              | N/A                                                  | $PSVersionTable                            |                                                 |
| with_env               | N/A                           | N/A                                                  | $env:FOO = 'bar'                           | export foo = "bar"                              |
| what                   |                               |                                                      |                                            |                                                 |
| where                  | where                         | Where                                                | Where-Object, where, "?" operator          |                                                 |
| which                  | N/A                           | N/A                                                  | N/A                                        | which                                           |
| wrap                   |                               |                                                      |                                            |                                                 |

`*` - these commands are part of the standard plugins