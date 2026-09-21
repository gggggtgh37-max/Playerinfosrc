# Player Info API — OB55 Fix

## Changes
- Updated outbound `ReleaseVersion` default from OB54 to OB55.
- Added `FF_RELEASE_VERSION` environment override.
- Removed hard-coded JWT credentials/endpoints from source code.
- Added per-region `JWT_URL_*` environment variables.
- Pinned protobuf to `6.30.0` to match the checked-in generated `data_pb2.py`.
- Added UID validation.
- Added clearer 503 response when a JWT endpoint is not configured.

## Vercel
Set the required `JWT_URL_<REGION>` environment variables in the Vercel project settings.
For example, set `JWT_URL_IND` to your own authorized JWT service endpoint.

Do not put real passwords, tokens, or API keys in the source code or ZIP.
