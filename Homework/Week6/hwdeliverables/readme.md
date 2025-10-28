How to set up and initialize terraform on your computer:

Depending on whether you use Windows or Mac, you use different package managers to install terraform. For Windows users; your package manager should be chocolatey, located at "https://github.com/rofoed01/scripts_chocolatey

For Mac users, use Homebrew, located at "https://github.com/rofoed01/scripts_homebrew".

To verify your terraform package is up to date, run '$ choco upgrade terraform' from an elevated shell on your machine, preferably gitbash. For Homebrew, run "$ brew update && brew upgrade"

Next, verify your AWS Agent is properly installed via '$ aws configure'. If this is not configured, additional assistance outside of this walkthrough is required.

Verify terraform is installed by running '$ terraform --version'.

If all is well at this point, choose a location for your terraform project.

Still in gitbash, create a directory if necessary via mkdir and cd into this directory.

The first file to create is your authentication file via '$ touch 0-auth.tf'.

After creating your .tf file, run the command '$ code .' to open VSCode.

Within VSCode, open a gitbash terminal.

The following script will check a few beneficial things like your AWS authentication, CLI configuration, chocolatey/homebrew and terraform version and download your .gitignore file:

'$ curl -O --ssl-no-revoke https://raw.githubusercontent.com/aaron-dm-mcdonald/aws-image-resizer/refs/heads/main/.gitignore'

The .gitignore file will be placed into the parent directory

Move it into your directory via '$ cp ../.gitignore .'

Save your 0-auth.tf file in VScode.

Run '$ terraform init' in your shell in VSCode.
