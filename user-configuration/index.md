# User Configuration Report on Debian

---

**Date:** 07/06/2025

**Project:** User, Group, and Permission Configuration with ACL on Debian

**Environment:**

* Debian GNU/Linux 12 (verified with `uname -a`)
* Local virtual machine

---

## ✅ Activities Performed

* Created groups: `dev_frontend`, `dev_backend`, `devops`, `lead`
* Created users: `alice`, `bob`, `carol`, and `dan`, each assigned to their respective secondary groups
* Set passwords for each user
* Edited the `sudoers` file to grant sudo privileges to the `devops` and `lead` groups
* Created shared directories: `/srv/proyectos` and `/srv/confidencial`
* Set standard permissions and ACLs:
  * `/srv/proyectos`: accessible by `devops`, `dev_frontend`, and `dev_backend`
  * `/srv/confidencial`: restricted exclusively to the `lead` group
* Applied the `setgid` bit on `/srv/proyectos` to ensure group inheritance
* Verified directory access with each user
* Tested `sudo` access with users `carol` and `dan`

---

## 📷 Evidence

* **Screenshot 1:** Groups created successfully (`groupadd`)  
  ![Groups created](images/01grupos.png)

* **Screenshot 2:** Users created and assigned to groups (`useradd`)  
  ![Users created](images/02usuarios.png)

* **Screenshot 3:** `sudo` privileges configured in `visudo`  
  ![Sudo configuration](images/03privilegios.png)

* **Screenshot 4:** Shared directories `/srv/proyectos` and `/srv/confidencial` created  
  ![Directories created](images/04directorios.png)

* **Screenshot 5:** Group permissions and ACLs applied (`getfacl`)  
  ![Group permissions and ACLs](images/05permisos_grupo.png)

* **Screenshot 6:** Access to `/srv/proyectos` and restriction to `/srv/confidencial` for different users  

  ![Access verified 1](images/06verificacion.png)  
  ![Access verified 2](images/07verificacion.png)  
  ![Access verified 3](images/08verificacion.png)  
  ![Access verified 4](images/09verificacion.png)

* **Screenshot 7:** `sudo` command execution by `carol` and `dan`  
  ![Sudo usage](images/11verificacion.png)
