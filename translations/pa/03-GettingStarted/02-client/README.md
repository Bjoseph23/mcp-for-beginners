<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "2342baa570312086fc19edcf41320250",
  "translation_date": "2025-06-17T15:37:15+00:00",
  "source_file": "03-GettingStarted/02-client/README.md",
  "language_code": "pa"
}
-->
ਪਿਛਲੇ ਕੋਡ ਵਿੱਚ ਅਸੀਂ:

- ਲਾਇਬ੍ਰੇਰੀਆਂ ਨੂੰ ਇੰਪੋਰਟ ਕੀਤਾ
- ਇੱਕ ਕਲਾਇੰਟ ਦਾ ਇੰਸਟੈਂਸ ਬਣਾਇਆ ਅਤੇ ਟਰਾਂਸਪੋਰਟ ਲਈ stdio ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਕਨੈਕਟ ਕੀਤਾ।
- ਪ੍ਰੌਂਪਟ, ਸਰੋਤ ਅਤੇ ਟੂਲਜ਼ ਨੂੰ ਲਿਸਟ ਕੀਤਾ ਅਤੇ ਉਹਨਾਂ ਸਾਰਿਆਂ ਨੂੰ ਇਨਵੋਕ ਕੀਤਾ।

ਇਹ ਹੈ, ਇੱਕ ਐਸਾ ਕਲਾਇੰਟ ਜੋ MCP ਸਰਵਰ ਨਾਲ ਗੱਲਬਾਤ ਕਰ ਸਕਦਾ ਹੈ।

ਅਗਲੇ ਅਭਿਆਸ ਭਾਗ ਵਿੱਚ ਅਸੀਂ ਹਰ ਕੋਡ ਸਨਿੱਪੇਟ ਨੂੰ ਵੱਖ-ਵੱਖ ਤੌਰ 'ਤੇ ਸਮਝਾਂਗੇ ਅਤੇ ਵਿਆਖਿਆ ਕਰਾਂਗੇ ਕਿ ਕੀ ਹੋ ਰਿਹਾ ਹੈ।

## ਅਭਿਆਸ: ਕਲਾਇੰਟ ਲਿਖਣਾ

ਜਿਵੇਂ ਉਪਰ ਕਿਹਾ ਗਿਆ ਹੈ, ਆਓ ਕੋਡ ਨੂੰ ਸਮਝਣ ਲਈ ਸਮਾਂ ਲਵਾਂ ਅਤੇ ਜੇ ਤੁਸੀਂ ਚਾਹੋ ਤਾਂ ਕੋਡ ਵੀ ਨਾਲ-ਨਾਲ ਲਿਖ ਸਕਦੇ ਹੋ।

### -1- ਲਾਇਬ੍ਰੇਰੀਆਂ ਇੰਪੋਰਟ ਕਰਨਾ

ਆਓ ਉਹ ਲਾਇਬ੍ਰੇਰੀਆਂ ਇੰਪੋਰਟ ਕਰੀਏ ਜਿਨ੍ਹਾਂ ਦੀ ਸਾਨੂੰ ਲੋੜ ਹੈ, ਸਾਨੂੰ ਕਲਾਇੰਟ ਅਤੇ ਸਾਡੇ ਚੁਣੇ ਹੋਏ ਟਰਾਂਸਪੋਰਟ ਪ੍ਰੋਟੋਕੋਲ, stdio, ਲਈ ਰੈਫਰੰਸ ਦੀ ਲੋੜ ਹੋਵੇਗੀ। stdio ਉਹ ਪ੍ਰੋਟੋਕੋਲ ਹੈ ਜੋ ਤੁਹਾਡੇ ਲੋਕਲ ਮਸ਼ੀਨ 'ਤੇ ਚੱਲਣ ਵਾਲੀਆਂ ਚੀਜ਼ਾਂ ਲਈ ਬਣਾਇਆ ਗਿਆ ਹੈ। SSE ਇੱਕ ਹੋਰ ਟਰਾਂਸਪੋਰਟ ਪ੍ਰੋਟੋਕੋਲ ਹੈ ਜਿਸਨੂੰ ਅਸੀਂ ਅਗਲੇ ਅਧਿਆਇਆਂ ਵਿੱਚ ਦਿਖਾਵਾਂਗੇ ਪਰ ਇਹ ਤੁਹਾਡਾ ਦੂਜਾ ਵਿਕਲਪ ਹੈ। ਹੁਣ ਲਈ, ਆਓ stdio ਨਾਲ ਹੀ ਅੱਗੇ ਵਧੀਏ।

ਆਓ ਇੰਸਟੈਂਸ਼ੀਏਸ਼ਨ ਵੱਲ ਵਧੀਏ।

### -2- ਕਲਾਇੰਟ ਅਤੇ ਟਰਾਂਸਪੋਰਟ ਦਾ ਇੰਸਟੈਂਸ ਬਣਾਉਣਾ

ਸਾਨੂੰ ਟਰਾਂਸਪੋਰਟ ਅਤੇ ਕਲਾਇੰਟ ਦੋਹਾਂ ਦਾ ਇੰਸਟੈਂਸ ਬਣਾਉਣਾ ਪਵੇਗਾ:

### -3- ਸਰਵਰ ਫੀਚਰਾਂ ਦੀ ਲਿਸਟਿੰਗ

ਹੁਣ ਸਾਡੇ ਕੋਲ ਇੱਕ ਕਲਾਇੰਟ ਹੈ ਜੋ ਪ੍ਰੋਗਰਾਮ ਚੱਲਣ 'ਤੇ ਕਨੈਕਟ ਹੋ ਸਕਦਾ ਹੈ। ਪਰ ਇਹ ਅਜੇ ਆਪਣੇ ਫੀਚਰਾਂ ਨੂੰ ਲਿਸਟ ਨਹੀਂ ਕਰਦਾ, ਤਾਂ ਆਓ ਹੁਣ ਇਹ ਕਰੀਏ:

ਵਧੀਆ, ਹੁਣ ਅਸੀਂ ਸਾਰੇ ਫੀਚਰ ਕੈਪਚਰ ਕਰ ਲਏ ਹਨ। ਹੁਣ ਸਵਾਲ ਇਹ ਹੈ ਕਿ ਅਸੀਂ ਇਹਨਾਂ ਨੂੰ ਕਦੋਂ ਵਰਤਾਂਗੇ? ਖੈਰ, ਇਹ ਕਲਾਇੰਟ ਕਾਫੀ ਸਧਾਰਣ ਹੈ, ਇਸਦਾ ਮਤਲਬ ਇਹ ਹੈ ਕਿ ਜਦੋਂ ਅਸੀਂ ਫੀਚਰਾਂ ਦੀ ਲੋੜ ਹੋਵੇਗੀ ਤਾਂ ਸਾਨੂੰ ਉਨ੍ਹਾਂ ਨੂੰ ਖੁਦ ਸਪਸ਼ਟ ਤੌਰ 'ਤੇ ਕਾਲ ਕਰਨਾ ਪਵੇਗਾ। ਅਗਲੇ ਅਧਿਆਇ ਵਿੱਚ ਅਸੀਂ ਇੱਕ ਹੋਰ ਅਡਵਾਂਸਡ ਕਲਾਇੰਟ ਬਣਾਵਾਂਗੇ ਜਿਸਦੇ ਕੋਲ ਆਪਣਾ ਵੱਡਾ ਭਾਸ਼ਾਈ ਮਾਡਲ, LLM, ਹੋਵੇਗਾ। ਪਰ ਹੁਣ ਲਈ, ਆਓ ਦੇਖੀਏ ਕਿ ਅਸੀਂ ਸਰਵਰ 'ਤੇ ਫੀਚਰਾਂ ਨੂੰ ਕਿਵੇਂ ਇਨਵੋਕ ਕਰ ਸਕਦੇ ਹਾਂ:

### -4- ਫੀਚਰਾਂ ਨੂੰ ਇਨਵੋਕ ਕਰਨਾ

ਫੀਚਰਾਂ ਨੂੰ ਇਨਵੋਕ ਕਰਨ ਲਈ ਸਾਨੂੰ ਇਹ ਯਕੀਨੀ ਬਣਾਉਣਾ ਪਵੇਗਾ ਕਿ ਅਸੀਂ ਸਹੀ ਆਰਗੂਮੈਂਟ ਦਿੱਤੇ ਹਨ ਅਤੇ ਕੁਝ ਮਾਮਲਿਆਂ ਵਿੱਚ ਉਸ ਚੀਜ਼ ਦਾ ਨਾਮ ਦਿੱਤਾ ਹੈ ਜਿਸਨੂੰ ਅਸੀਂ ਇਨਵੋਕ ਕਰਨਾ ਚਾਹੁੰਦੇ ਹਾਂ।

### -5- ਕਲਾਇੰਟ ਚਲਾਉਣਾ

ਕਲਾਇੰਟ ਚਲਾਉਣ ਲਈ, ਟਰਮੀਨਲ ਵਿੱਚ ਹੇਠਾਂ ਦਿੱਤਾ ਕਮਾਂਡ ਟਾਈਪ ਕਰੋ:

## ਅਸਾਈਨਮੈਂਟ

ਇਸ ਅਸਾਈਨਮੈਂਟ ਵਿੱਚ, ਤੁਸੀਂ ਜੋ ਕੁਝ ਸਿੱਖਿਆ ਹੈ ਉਸਦੀ ਵਰਤੋਂ ਕਰਦੇ ਹੋਏ ਆਪਣਾ ਖੁਦ ਦਾ ਕਲਾਇੰਟ ਬਣਾਉਗੇ।

ਇੱਥੇ ਇੱਕ ਸਰਵਰ ਹੈ ਜਿਸਨੂੰ ਤੁਸੀਂ ਆਪਣੇ ਕਲਾਇੰਟ ਕੋਡ ਰਾਹੀਂ ਕਾਲ ਕਰਨਾ ਹੈ, ਦੇਖੋ ਕਿ ਕੀ ਤੁਸੀਂ ਸਰਵਰ ਵਿੱਚ ਹੋਰ ਫੀਚਰ ਜੋੜ ਕੇ ਇਸਨੂੰ ਹੋਰ ਦਿਲਚਸਪ ਬਣਾ ਸਕਦੇ ਹੋ।

## ਹੱਲ

[Solution](./solution/README.md)

## ਮੁੱਖ ਗੱਲਾਂ

ਇਸ ਅਧਿਆਇ ਵਿੱਚ ਕਲਾਇੰਟਾਂ ਬਾਰੇ ਮੁੱਖ ਗੱਲਾਂ ਇਹ ਹਨ:

- ਸਰਵਰ 'ਤੇ ਫੀਚਰਾਂ ਦੀ ਖੋਜ ਅਤੇ ਇਨਵੋਕੇਸ਼ਨ ਦੋਹਾਂ ਲਈ ਵਰਤੇ ਜਾ ਸਕਦੇ ਹਨ।
- ਇੱਕ ਕਲਾਇੰਟ ਆਪਣੇ ਆਪ ਨੂੰ ਸ਼ੁਰੂ ਕਰ ਸਕਦਾ ਹੈ ਜਿਵੇਂ ਕਿ ਇਸ ਅਧਿਆਇ ਵਿੱਚ ਕੀਤਾ ਗਿਆ ਹੈ, ਪਰ ਕਲਾਇੰਟ ਚੱਲ ਰਹੇ ਸਰਵਰਾਂ ਨਾਲ ਵੀ ਕਨੈਕਟ ਹੋ ਸਕਦਾ ਹੈ।
- ਇਹ ਸਰਵਰ ਦੀਆਂ ਸਮਰੱਥਾਵਾਂ ਦੀ ਜਾਂਚ ਕਰਨ ਦਾ ਇੱਕ ਵਧੀਆ ਤਰੀਕਾ ਹੈ, ਇੰਸਪੈਕਟਰ ਵਰਗੀਆਂ ਵਿਕਲਪਾਂ ਦੇ ਨਾਲ।

## ਵਾਧੂ ਸਰੋਤ

- [MCP ਵਿੱਚ ਕਲਾਇੰਟ ਬਣਾਉਣਾ](https://modelcontextprotocol.io/quickstart/client)

## ਨਮੂਨੇ

- [Java ਕੈਲਕੁਲੇਟਰ](../samples/java/calculator/README.md)
- [.Net ਕੈਲਕੁਲੇਟਰ](../../../../03-GettingStarted/samples/csharp)
- [JavaScript ਕੈਲਕੁਲੇਟਰ](../samples/javascript/README.md)
- [TypeScript ਕੈਲਕੁਲੇਟਰ](../samples/typescript/README.md)
- [Python ਕੈਲਕੁਲੇਟਰ](../../../../03-GettingStarted/samples/python)

## ਅਗਲਾ ਕੀ ਹੈ

- ਅਗਲਾ: [LLM ਨਾਲ ਕਲਾਇੰਟ ਬਣਾਉਣਾ](/03-GettingStarted/03-llm-client/README.md)

**ਅਸਵੀਕਾਰੋक्ति**:  
ਇਸ ਦਸਤਾਵੇਜ਼ ਦਾ ਅਨੁਵਾਦ AI ਅਨੁਵਾਦ ਸੇਵਾ [Co-op Translator](https://github.com/Azure/co-op-translator) ਦੀ ਵਰਤੋਂ ਕਰਕੇ ਕੀਤਾ ਗਿਆ ਹੈ। ਜਦੋਂ ਕਿ ਅਸੀਂ ਸਹੀਤਾ ਲਈ ਯਤਨਸ਼ੀਲ ਹਾਂ, ਕਿਰਪਾ ਕਰਕੇ ਜਾਣੋ ਕਿ ਸਵੈਚਾਲਿਤ ਅਨੁਵਾਦਾਂ ਵਿੱਚ ਗਲਤੀਆਂ ਜਾਂ ਅਸਮਰੱਥਤਾਵਾਂ ਹੋ ਸਕਦੀਆਂ ਹਨ। ਮੂਲ ਦਸਤਾਵੇਜ਼ ਆਪਣੀ ਮੂਲ ਭਾਸ਼ਾ ਵਿੱਚ ਅਧਿਕਾਰਤ ਸਰੋਤ ਮੰਨਿਆ ਜਾਣਾ ਚਾਹੀਦਾ ਹੈ। ਮਹੱਤਵਪੂਰਨ ਜਾਣਕਾਰੀ ਲਈ, ਪੇਸ਼ੇਵਰ ਮਨੁੱਖੀ ਅਨੁਵਾਦ ਦੀ ਸਿਫਾਰਸ਼ ਕੀਤੀ ਜਾਂਦੀ ਹੈ। ਅਸੀਂ ਇਸ ਅਨੁਵਾਦ ਦੀ ਵਰਤੋਂ ਤੋਂ ਉਤਪੰਨ ਕਿਸੇ ਵੀ ਗਲਤਫਹਮੀ ਜਾਂ ਭ੍ਰਮ ਲਈ ਜ਼ਿੰਮੇਵਾਰ ਨਹੀਂ ਹਾਂ।