# Notes to be better user of powershell   

## 1. Get-Help
Get-Help is your friend. It is the best way to learn about a command.
    
    ```powershell
    Get-Help Get-Process

    Get-Help Get-Process -Examples
    ```

# search
https://shellgeek.com/powershell-search-for-files/#PowerShell_find_file_using_Get-ChildItem


Get-ChildItem -Path "$HOME\..\..\Volumes\kt-fs1\LabelOutputs\" -Filter "*.dat" -Recurse | select-string -pattern '(?s)(%2_2.2%).+?(07/10/2023)' 

$folderPath = "C:\Your\Folder\Path"
$string1 = "first string"
$string2 = "second string"

Get-ChildItem -Path $folderPath -File | ForEach-Object {
    $filePath = $_.FullName
    $fileContent = Get-Content -Path $filePath -Raw
    if ($fileContent -match $string1 -and $fileContent -match $string2) {
        Write-Host "Both strings found in file: $filePath"
    }
}

(PowerShell playlist)[https://www.youtube.com/playlist?list=PLvmwu6WYeFdgw8LJ2VUhveL86qEtY7TXT]