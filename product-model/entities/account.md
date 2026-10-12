---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "packages/core/src/Entity/User.php"
    }
  ],
  "relations": [
    {
      "entity": "page",
      "verb": "creates",
      "cardinality": "one-to-many"
    },
    {
      "entity": "redirection",
      "verb": "creates",
      "cardinality": "one-to-many"
    },
    {
      "entity": "page",
      "verb": "edits",
      "cardinality": "one-to-many"
    },
    {
      "entity": "redirection",
      "verb": "edits",
      "cardinality": "one-to-many"
    },
    {
      "entity": "browser-draft",
      "verb": "owns",
      "cardinality": "one-to-many"
    }
  ],
  "domain": "users"
}
---

# Account

The profile and credentials shared by whichever shipped role its holder occupies. Required password completion masks effective ordinary roles. Stored password material is never disclosed as a password.

## Information kept

- **Reference** — The subject identity used to select this instance.
- **Email** — The retained email for this account.
- **Username** — The stored display username; it is distinct from the email used as the account identifier.
- **Interface locale** — The account’s chosen interface locale; content locale is stored independently.
- **Roles** — The assigned shipped role values; effective roles are masked while password change is required.
- **Password** — Stored password material used for credential verification, never returned as a plain password.
- **API token** — The optional credential used by the CMS API; candidate form changes are persisted on save.
- **Password change required** — Whether ordinary account privileges are masked pending password completion.
- **Created at** — The retained created at for this account.
- **Custom properties** — The retained named extension values, accepted or merged only through the supported entry path.
