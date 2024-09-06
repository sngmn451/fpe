# TypeScript Format-Preserving Encryption

Build with Claude.ai, document with Codeium.

## Usage

You need `key` and `tweak` to use this function, you may generate one using [nanoid](https://uuid.rocks/nanoid)

Encrypt

```typescript
encrypt(idString, key, tweak);
```

Decrypt

```typescript
decrypt(String(encryptedId), key, tweak);
```

EncryptId

```typescript
encryptId(Number(c.req.param("id")), key, tweak);
```

DecryptId

```typescript
decryptId(c.req.param("id"), key, tweak);
```

## Performance

Tested with 1M generated IDs (1-1,000,000), including encryption and decryption of all IDs (run on Mac Mini M1, 16GB RAM).

Times shown below are in ms.

```json
{
  "totalIds": "1,000,000",
  "generatedTime": 76,
  "encryptedTime": 1863,
  "decryptedTime": 1803
}
```

## Security?

No idea, zero knowledge at all.

Feedback or PRs are welcome
