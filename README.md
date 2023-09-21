# Nuxt Supabase Demonstration

## Prerequisites

The following tools are installed

- supabase CLI

## Init supabase project

> This step is at the beginning of project creation. You shouldn't need use this steps.
> We put here only for documentation purposes

```bash
      supabase init
```

## Setup supabase

- Generate access_token at [here](https://supabase.com/dashboard/account/tokens)
- then `supabase login`

## Generate Supabase edge functions

```bash
      supabase functions new <func_name>
```

## Deploy supbase edge functions

```bash
      SUPABASE_ACCESS_TOKEN=xxx supabase functions deploy <func_name> --project-ref <project_ref_id>
```

## Create database migrations

- Create/Update database table in the table editor
- Generate migration
  ```bash
      supabase db diff --use-migra -f <output_migration_file_name>
  ```
- To verify that the new migration does not generate errors.
  ```bash
    supabase db reset
  ```

## Run database migrations and seed database

```bash
      supabase db reset
```
