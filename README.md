@VIA-azure.js;VIA AMI .AI>

# structual-foundation
Structuring Adv.node

runs-on: self-hosted

"publishConfig": { "registry": "https://npm.pkg.github.com/" }
npm login --registry=https://npm.pkg.github.com/
npm publish

mkdir actions-runner; cd actions-runner
Add-Type -AssemblyName System.IO.Compression.FileSystem ; [System.IO.Compression.ZipFile]::ExtractToDirectory("$PWD/actions-runner-win-x64-2.169.1.zip", "$PWD")
Invoke-WebRequest -Uri https://github.com/actions/runner/releases/download/v2.169.1/actions-runner-win-x64-2.169.1.zip -OutFile actions-runner-win-x64-2.169.1.zip
