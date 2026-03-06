# Prism School Registry

A community-maintained list of institutional AWS portal URLs for academic researchers.

When researchers at universities launch [Prism](https://github.com/scttfrdmn/prism) for the first time without AWS credentials, Prism can direct them to their institution's portal to obtain a sponsored account.

## Usage

```bash
# Find your institution
prism schools search stanford
prism schools search "university of washington"

# View all registered institutions
prism schools list

# Get portal URL and setup instructions
prism schools info mit
```

## Contributing

If your institution provides AWS accounts to researchers and isn't listed here, please [open an issue](https://github.com/scttfrdmn/prism-school-registry/issues/new/choose) using the **Register Institution** template.

For corrections or updates to existing entries, open a pull request against `schools.yaml`.

## Schema

Each entry in `schools.yaml` has these fields:

| Field | Required | Description |
|-------|----------|-------------|
| `id` | ✅ | Short unique identifier (lowercase, hyphens ok) |
| `name` | ✅ | Full institution name |
| `short_name` | | Common abbreviation |
| `country` | ✅ | ISO 3166-1 alpha-2 country code |
| `state` | | US state abbreviation (US institutions) |
| `email_domains` | ✅ | List of institutional email domains |
| `aws_portal_url` | ✅ | URL where researchers request AWS accounts |
| `aws_program` | ✅ | One of: `enterprise`, `educate`, `research_credits`, `research`, `other` |
| `notes` | | Brief guidance for researchers |
| `verified` | | Whether the URL has been verified recently |
| `last_verified` | | Month last verified (YYYY-MM format) |

## License

Content is available under [CC0 1.0 Universal](LICENSE).
