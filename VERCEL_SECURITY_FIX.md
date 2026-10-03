# Vercel security fix

This package pins TanStack Start to the security-patched release `@tanstack/react-start@1.168.60` and forces `@tanstack/start-server-core@1.169.39` or later through npm overrides.

TanStack disclosed CVE-2026-102989 on September 30, 2026. Affected React Start versions are >=1.143.12 and <1.168.60; affected Start Server Core versions are >=1.143.12 and <1.169.39. After updating, redeploy the application.

Vercel should be allowed to generate a fresh lockfile during installation. Do not commit an old lockfile that resolves the vulnerable versions.
