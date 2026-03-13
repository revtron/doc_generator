
# DevOps Handover Document (Ansible + Jinja2)

This repository/project is designed to generate a structured **handover document** using **Ansible** and **Jinja2 templates**. It consolidates key information such as CI/CD flow, app build flow, and component access.

## 📁 Folder Structure

```

.
├── vars/
│   ├── app_build_flow.yml         # Info about app build process
│   ├── cicd.yml                   # Info about CI/CD flow
│   └── component_access.yml       # Info about component access
│
├── templates/
│   ├── access.md.j2               # Jinja2 template for access info
│   ├── app_build_flow.md.j2       # Jinja2 template for build flow
│   ├── cicd.md.j2                 # Jinja2 template for CI/CD flow
│   └── component.md.j2            # Jinja2 template for component overview
│
├── output/
│   ├── access.md                  # Final generated access info
│   ├── app_build_flow.md         # Final generated build flow doc
│   ├── cicd.md                   # Final generated CI/CD doc
│   └── component.md              # Final generated component doc
│
├── handover.yml                   # Main Ansible playbook
└── README.md                      # This file

```

---

## ✅ What You Need to Fill

Inside the `vars/` directory, ensure the following files are filled with the required data in YAML format:

- `app_build_flow.yml` → Structure and steps for building and releasing the app.
- `cicd.yml` → Details about your CI/CD pipeline, tools, triggers, etc.
- `component_access.yml` → Component-level access control, roles, credentials, etc.

---

## ▶️ How to Generate the Handover Document

Run the following command:

```bash
ansible-playbook handover.yml
```

This will read the variable files from the `vars/` directory and generate final markdown documents inside the `output/` directory using the Jinja2 templates in `templates/`.

---

## 📄 Final Outputs

After execution, the following documents will be available under the `output/` folder:

* `access.md`
* `app_build_flow.md`
* `cicd.md`
* `component.md`

These can be directly used as part of your onboarding or system handover documentation.

---


