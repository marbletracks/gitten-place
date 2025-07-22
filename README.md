# 📱 Mobile Git Deployment Panel for https://www.marbletrack3.com 

This project provides a **mobile-friendly web interface** for https://github.com/marbletracks/db.marbletrack3.com hosted on [DreamHost Shared Hosting](https://www.dreamhost.com/). It allows you to:

- ✅ Pull the latest changes from your Git repository
- ✅ Switch to a different remote branch
- ✅ Roll back to a previous commit
- ✅ Use it securely from your phone via HTTPS and basic auth

---

## 🚀 Features

- PHP-based, works on DreamHost shared hosting
- Lightweight UI with [Picnic CSS](https://picnicss.com/)
- Secure access via cookies
- Dropdown for selecting branches from the remote (e.g., `origin/main`, `origin/dev`)
- Logs recent commits and shows Git output for actions

---

## 📁 Installation

1. **Clone or copy the files** into a secure subfolder of your website, e.g. `/home/dh_user/example.com/wwwroot/admin/git/`.

2. create a symlink of `classes/Config.php` --> `../../classes/Config.php`



4. Visit your panel at:

https://db.marbketrack3.com/admin/git




---

📱 Usage

Pull Latest: Updates the current branch to the latest from origin.

Switch Branch: Select a branch from the dropdown and switch to it.

Rollback: Enter a short commit hash to reset the repo to that state.


> 🔐 Ensure you're using HTTPS and login with same credentials as base website.




---

⚠️ Notes

This will hopefully be nestable.  `/domain.com/wwwroot/git/git/git`

The script uses shell_exec() and assumes your Git repo is already cloned and authorized via SSH.



---

🛠️ Todo / Ideas

[ ] Add confirmation before rollback

[ ] Show file diffs for commit rollback

[ ] Log deployment actions

[ ] Deploy via webhook (optional alternative)







---

## 🚀 Features

- Lightweight custom templating (no Twig, Blade, or Smarty)
- Admin dashboard scaffold
- Built-in layout nesting (`grabTheGoods()`)
- Styled with light blues and page panels
- uses base website for logins

---

## 🔧 Setup (with DreamHost Deployment)

1. **Set up a DreamHost new user account:**
   - Clone [thunderrabbit/new-DH-user-account](https://github.com/thunderrabbit/new-DH-user-account)

2. **Set your domain's Web Directory in DreamHost panel:**
   - e.g. `/home/dh_user/example.com/wwwroot`

3. **Clone this repo locally** into  directory `/home/thunderrabbit/work/gitcrackin`

4. **Configure your deploy script:**
   - Edit `scp_files_to_dh.sh` to point to your DH username and target path.

5. **Clone this repo server-side**:
   - Clone to `/home/dh_user/example.com/wwwroot/admin/git/`

6. **Deploy with `scp_files_to_dh.sh`** or manually sync files.
