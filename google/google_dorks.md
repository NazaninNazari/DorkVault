# Google Dorks
A collection of Google search dorks for authorized reconnaissance, exposure discovery, and security research.
Replace target-specific terms where appropriate. Use these queries only against systems, domains, and organizations that are explicitly within your authorized scope.

---

## 1. Directory Listing & Indexing
intitle:"index of" inurl:ftp intext:admin
intitle:"index of" "system/config"
intitle:"index of" "admin/config"
"index of" "/config/sql"
intitle:"index of" "api/admin"
intitle:"index of" "tinyfilemanager.php"
intitle:"index of" "test/storage/framework/sessions/"
intitle:"index of" "symfony/config"
intitle:"index of" "graphql/subscription"
intitle:"index of" "/admin/backup"
intitle:"index of" "admin/json"
intitle:"index of" "/admin_backup"
intitle:"index of" "git-jira-log"
intitle:"index of" db.frm
intitle:"index of" "/db_backups/"
intitle:"index of" "common.crt" OR "ca.crt"
intitle:"index of" "global.asa"
intitle:"index of" "proxy.pac" OR "proxy.pac.bak"
intitle:"index of" "MySQL-Router"
intitle:"index of" "owncloud/config/*"
"index of" "backup.sql"
"index of" "settings.json"
"index of" "api_key"
"index of" "server-status"

---

## 2. Configuration & Sensitive Files
filetype:ini "password" site:org
filetype:txt "credentials" site:gov
filetype:yaml "secret_key" -examples
filetype:key "PRIVATE KEY"
filetype:pem "PRIVATE KEY"
filetype:json "db_password" -github
filetype:db "database" site:org
filetype:conf "db_user" site:org
filetype:config "ftp" site:gov
filetype:xml "web.config" site:edu
filetype:env "SECRET_KEY"
filetype:json "api_token"
filetype:txt "api_secret"

---

## 3. Logs & Debug Information
filetype:log "debug" "error"
filetype:log "Stack trace" site:edu
filetype:log "unable to connect"
filetype:log "authentication failed"

---

## 4. Backups & Database Files
filetype:sql "INSERT INTO" "VALUES" site:edu
filetype:dump "database" site:gov
filetype:db "database" site:org
"index of" "backup.sql"

---

## 5. Credentials & API Secrets
filetype:ini "password" site:org
filetype:json "db_password" -github
filetype:env "SECRET_KEY"
filetype:json "api_token"
filetype:txt "api_secret"
site:pastebin.com "password"
site:github.com "SECRET_KEY"
site:gitlab.com "PRIVATE_KEY"
site:bitbucket.org "db_password"

---

## 6. Administrative Interfaces
"admin login" filetype:php
"admin dashboard" "login"
"index of" "server-status"
filetype:php "mysql_connect" site:gov

---

## 7. Sensitive Documents
filetype:pdf "not for distribution" site:gov
filetype:xlsx "confidential report" site:edu
filetype:doc "salary" "employee"
filetype:docx "restricted access"
filetype:xlsx "username" "password" site:gov
filetype:xls "username" "password" site:gov
filetype:xlsx "username" site:gov
filetype:xls "username" site:gov
filetype:xlsx "database" site:gov
filetype:xls "database" site:gov
filetype:xlsx "financial" site:gov
filetype:xls "financial" site:gov
filetype:xlsx "password" site:gov
filetype:xls "password" site:gov

---

## 8. Cloud Storage & Code Hosting
site:dropbox.com "password"
site:box.com "confidential"
site:drive.google.com "important"
site:onedrive.live.com "restricted"
site:pastebin.com "password"
site:github.com "SECRET_KEY"
site:gitlab.com "PRIVATE_KEY"
site:bitbucket.org "db_password"

---

## Usage Notes
- Use these queries only for authorized security research.
- Apply domain, organization, or other scope restrictions whenever appropriate.
- Search results can contain false positives and outdated information.
- Do not access, download, authenticate to, or use exposed credentials without explicit authorization.
- Treat potentially sensitive documents, credentials, logs, and keys as confidential.
- Do not disclose sensitive values publicly.
- Follow the applicable bug bounty rules and responsible disclosure policy.

---

## Safety & Scope
A search result is not automatically a vulnerability.
Before considering a finding, verify:
1. Ownership of the resource.
2. Whether it is within the authorized scope.
3. Whether the exposure is actually accessible.
4. Whether sensitive information is genuinely exposed.
5. Whether there is a meaningful security impact.

Minimize interaction with discovered resources and avoid unnecessary access to sensitive information.