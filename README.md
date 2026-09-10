# Supabase stack for Wodby

Self-hosted Supabase with dedicated PostgreSQL, Auth, REST, Realtime, Storage and Studio. Each app environment runs one Supabase project using the tested self-hosted/v0.8.1 component bundle.

Supply the application site URL, sender address and SMTP integration when creating an environment. Wodby routes HTTPS to the Supabase gateway. Studio uses its generated dashboard password; client applications use the public URL and publishable API key.

The default stack uses persistent filesystem storage and single-replica workloads. Optional S3 storage requires an existing bucket and an integration exposing the documented native AWS variables. Edge Functions, connection pooling, analytics and database HA are not included in the initial version.

Back up the database, required encryption keys, source tokens and stored objects together. Stop application writers when establishing a coordinated recovery point. Environment copying preserves credentials; rotate client-facing keys deliberately after a copy when required. Upgrades should follow tested Supabase bundles, and a Helm rollback does not undo database migrations.

<!-- wodby:generated:start -->
<!-- wodby:generated:end -->
