<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "d88dbf928fa0f159b82312e9a6757ba0",
  "translation_date": "2025-06-18T09:23:59+00:00",
  "source_file": "04-PracticalImplementation/README.md",
  "language_code": "tl"
}
-->
# Praktikal na Pagpapatupad

Ang praktikal na pagpapatupad ang nagiging konkretong patunay ng kapangyarihan ng Model Context Protocol (MCP). Bagaman mahalaga ang pag-unawa sa teorya at arkitektura sa likod ng MCP, ang tunay na halaga ay lumilitaw kapag inilalapat mo ang mga konseptong ito para bumuo, subukan, at i-deploy ang mga solusyon na tumutugon sa mga totoong problema sa mundo. Pinag-uugnay ng kabanatang ito ang pagitan ng konseptwal na kaalaman at aktwal na pag-develop, na ginagabayan ka sa proseso ng paggawa ng mga aplikasyon na nakabase sa MCP.

Kung ikaw man ay gumagawa ng mga matatalinong assistant, nag-iintegrate ng AI sa mga daloy ng trabaho sa negosyo, o bumubuo ng mga custom na kasangkapan para sa pagproseso ng datos, nagbibigay ang MCP ng isang flexible na pundasyon. Ang disenyo nito na hindi nakadepende sa wika at ang mga opisyal na SDK para sa mga kilalang programming languages ay ginagawang accessible ito sa malawak na hanay ng mga developer. Sa pamamagitan ng paggamit ng mga SDK na ito, maaari kang mabilis na gumawa ng prototype, mag-iterate, at mag-scale ng iyong mga solusyon sa iba't ibang platform at kapaligiran.

Sa mga sumusunod na bahagi, makikita mo ang mga praktikal na halimbawa, sample code, at mga estratehiya sa deployment na nagpapakita kung paano ipatupad ang MCP sa C#, Java, TypeScript, JavaScript, at Python. Malalaman mo rin kung paano i-debug at subukan ang iyong mga MCP server, pamahalaan ang mga API, at i-deploy ang mga solusyon sa cloud gamit ang Azure. Ang mga hands-on na resources na ito ay dinisenyo upang pabilisin ang iyong pagkatuto at tulungan kang kumpiyansang bumuo ng matibay at handang gamitin sa produksyon na mga aplikasyon ng MCP.

## Pangkalahatang-ideya

Ang araling ito ay nakatuon sa mga praktikal na aspeto ng pagpapatupad ng MCP sa iba't ibang programming languages. Tatalakayin natin kung paano gamitin ang MCP SDKs sa C#, Java, TypeScript, JavaScript, at Python upang bumuo ng matibay na mga aplikasyon, i-debug at subukan ang MCP servers, at gumawa ng mga reusable na resources, prompts, at tools.

## Mga Layunin sa Pagkatuto

Sa pagtatapos ng araling ito, magagawa mong:
- Ipatupad ang mga solusyon ng MCP gamit ang opisyal na SDKs sa iba't ibang programming languages
- Sistematikong i-debug at subukan ang mga MCP server
- Gumawa at gumamit ng mga tampok ng server (Resources, Prompts, at Tools)
- Magdisenyo ng epektibong mga MCP workflow para sa mga komplikadong gawain
- I-optimize ang mga pagpapatupad ng MCP para sa performance at pagiging maaasahan

## Mga Opisyal na SDK Resources

Nagbibigay ang Model Context Protocol ng mga opisyal na SDK para sa iba't ibang wika:

- [C# SDK](https://github.com/modelcontextprotocol/csharp-sdk)
- [Java SDK](https://github.com/modelcontextprotocol/java-sdk)
- [TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk)
- [Python SDK](https://github.com/modelcontextprotocol/python-sdk)
- [Kotlin SDK](https://github.com/modelcontextprotocol/kotlin-sdk)

## Paggamit ng MCP SDKs

Ang seksyong ito ay naglalaman ng mga praktikal na halimbawa ng pagpapatupad ng MCP sa iba't ibang programming languages. Makikita mo ang sample code sa `samples` directory na inayos ayon sa wika.

### Mga Available na Sample

Kasama sa repository ang [mga sample na pagpapatupad](../../../04-PracticalImplementation/samples) sa mga sumusunod na wika:

- [C#](./samples/csharp/README.md)
- [Java](./samples/java/containerapp/README.md)
- [TypeScript](./samples/typescript/README.md)
- [JavaScript](./samples/javascript/README.md)
- [Python](./samples/python/README.md)

Bawat sample ay nagpapakita ng mga pangunahing konsepto at pattern ng MCP para sa partikular na wika at ecosystem.

## Pangunahing Mga Tampok ng Server

Maaaring ipatupad ng mga MCP server ang alinman o kombinasyon ng mga sumusunod na tampok:

### Resources
Nagbibigay ang mga resources ng konteksto at datos para magamit ng user o AI model:
- Mga repositoryo ng dokumento
- Mga knowledge base
- Mga structured data source
- Mga file system

### Prompts
Ang mga prompts ay mga templated na mensahe at workflow para sa mga user:
- Mga paunang gawa na template ng pag-uusap
- Mga gabay na pattern ng interaksyon
- Mga espesyal na estruktura ng diyalogo

### Tools
Ang mga tools ay mga function na pinapatakbo ng AI model:
- Mga utility para sa pagproseso ng datos
- Integrasyon ng external API
- Mga kakayahan sa komputasyon
- Functionality para sa paghahanap

## Mga Sample na Pagpapatupad: C#

Ang opisyal na C# SDK repository ay naglalaman ng ilang mga sample na pagpapatupad na nagpapakita ng iba't ibang aspeto ng MCP:

- **Basic MCP Client**: Simpleng halimbawa kung paano gumawa ng MCP client at tumawag ng mga tool
- **Basic MCP Server**: Minimal na pagpapatupad ng server na may pangunahing tool registration
- **Advanced MCP Server**: Kumpletong server na may tool registration, authentication, at error handling
- **ASP.NET Integration**: Mga halimbawa ng integrasyon sa ASP.NET Core
- **Tool Implementation Patterns**: Iba't ibang pattern para sa pagpapatupad ng mga tool na may iba't ibang antas ng komplikasyon

Ang MCP C# SDK ay nasa preview pa at maaaring magbago ang mga API. Patuloy naming ia-update ang blog na ito habang umuunlad ang SDK.

### Pangunahing Mga Tampok
- [C# MCP Nuget ModelContextProtocol](https://www.nuget.org/packages/ModelContextProtocol)

- Pagtatayo ng iyong [unang MCP Server](https://devblogs.microsoft.com/dotnet/build-a-model-context-protocol-mcp-server-in-csharp/).

Para sa kumpletong mga sample ng pagpapatupad sa C#, bisitahin ang [opisyal na C# SDK samples repository](https://github.com/modelcontextprotocol/csharp-sdk)

## Sample na pagpapatupad: Java Implementation

Nagbibigay ang Java SDK ng matibay na mga opsyon para sa pagpapatupad ng MCP na may enterprise-grade na mga tampok.

### Pangunahing Mga Tampok

- Integrasyon sa Spring Framework
- Malakas na type safety
- Suporta sa reactive programming
- Komprehensibong error handling

Para sa kumpletong sample ng Java implementation, tingnan ang [MCPSample.java](../../../04-PracticalImplementation/samples/java/MCPSample.java) sa samples directory.

## Sample na pagpapatupad: JavaScript Implementation

Nagbibigay ang JavaScript SDK ng magaan at flexible na paraan para sa pagpapatupad ng MCP.

### Pangunahing Mga Tampok

- Suporta sa Node.js at browser
- Promise-based na API
- Madaling integrasyon sa Express at iba pang frameworks
- Suporta sa WebSocket para sa streaming

Para sa kumpletong sample ng JavaScript implementation, tingnan ang [mcp_sample.js](../../../04-PracticalImplementation/samples/javascript/mcp_sample.js) sa samples directory.

## Sample na pagpapatupad: Python Implementation

Nag-aalok ang Python SDK ng Pythonic na paraan ng pagpapatupad ng MCP na may mahusay na integrasyon sa mga ML framework.

### Pangunahing Mga Tampok

- Async/await na suporta gamit ang asyncio
- Integrasyon sa Flask at FastAPI
- Simpleng tool registration
- Native na integrasyon sa mga kilalang ML libraries

Para sa kumpletong sample ng Python implementation, tingnan ang [mcp_sample.py](../../../04-PracticalImplementation/samples/python/mcp_sample.py) sa samples directory.

## Pamamahala ng API

Ang Azure API Management ay isang mahusay na solusyon kung paano natin mapoprotektahan ang mga MCP Server. Ang ideya ay maglagay ng Azure API Management instance sa harap ng iyong MCP Server at hayaang ito ang humawak ng mga tampok na malamang na gusto mo tulad ng:

- rate limiting
- token management
- monitoring
- load balancing
- seguridad

### Azure Sample

Narito ang isang Azure Sample na eksaktong gumagawa nito, ibig sabihin [gumagawa ng MCP Server at pinoprotektahan ito gamit ang Azure API Management](https://github.com/Azure-Samples/remote-mcp-apim-functions-python).

Tingnan kung paano nangyayari ang authorization flow sa larawan sa ibaba:

![APIM-MCP](https://github.com/Azure-Samples/remote-mcp-apim-functions-python/blob/main/mcp-client-authorization.gif?raw=true)

Sa larawang nasa itaas, nangyayari ang mga sumusunod:

- Nagaganap ang Authentication/Authorization gamit ang Microsoft Entra.
- Ang Azure API Management ay gumaganap bilang gateway at gumagamit ng mga polisiya para idirekta at pamahalaan ang trapiko.
- Ang Azure Monitor ay nagtatala ng lahat ng request para sa karagdagang pagsusuri.

#### Daloy ng Authorization

Tingnan natin nang mas detalyado ang daloy ng authorization:

![Sequence Diagram](https://github.com/Azure-Samples/remote-mcp-apim-functions-python/blob/main/infra/app/apim-oauth/diagrams/images/mcp-client-auth.png?raw=true)

#### MCP authorization specification

Alamin pa ang tungkol sa [MCP Authorization specification](https://modelcontextprotocol.io/specification/2025-03-26/basic/authorization#2-10-third-party-authorization-flow)

## I-deploy ang Remote MCP Server sa Azure

Tingnan natin kung kaya nating i-deploy ang sample na nabanggit kanina:

1. I-clone ang repo

    ```bash
    git clone https://github.com/Azure-Samples/remote-mcp-apim-functions-python.git
    cd remote-mcp-apim-functions-python
    ```

2. Magrehistro gamit ang `Microsoft.App` resource provider.
    * If you are using Azure CLI, run `az provider register --namespace Microsoft.App --wait`.
    * If you are using Azure PowerShell, run `Register-AzResourceProvider -ProviderNamespace Microsoft.App`. Then run `(Get-AzResourceProvider -ProviderNamespace Microsoft.App).RegistrationState` at maghintay ng ilang sandali para masigurong kumpleto na ang pagrehistro.

3. Patakbuhin ang [azd](https://aka.ms/azd) command na ito para i-provision ang api management service, function app (kasama ang code) at lahat ng iba pang kinakailangang Azure resources

    ```shell
    azd up
    ```

    Ang mga command na ito ay dapat mag-deploy ng lahat ng cloud resources sa Azure

### Pagsubok ng iyong server gamit ang MCP Inspector

1. Sa isang **bagong terminal window**, i-install at patakbuhin ang MCP Inspector

    ```shell
    npx @modelcontextprotocol/inspector
    ```

    Makikita mo ang interface na katulad ng:

    ![Connect to Node inspector](../../../translated_images/connect.141db0b2bd05f096fb1dd91273771fd8b2469d6507656c3b0c9df4b3c5473929.tl.png)

2. CTRL click upang buksan ang MCP Inspector web app mula sa URL na ipinapakita ng app (hal. http://127.0.0.1:6274/#resources)
3. Itakda ang transport type sa `SSE`
1. Set the URL to your running API Management SSE endpoint displayed after `azd up` at **Connect**:

    ```shell
    https://<apim-servicename-from-azd-output>.azure-api.net/mcp/sse
    ```

5. **Ilista ang mga Tools**. I-click ang isang tool at **Run Tool**.

Kung nagtagumpay ang lahat ng mga hakbang, dapat ay nakakonekta ka na ngayon sa MCP server at nagawa mong tawagan ang isang tool.

## MCP servers para sa Azure

[Remote-mcp-functions](https://github.com/Azure-Samples/remote-mcp-functions-dotnet): Ang set ng mga repository na ito ay mga quickstart template para sa paggawa at pag-deploy ng custom remote MCP (Model Context Protocol) servers gamit ang Azure Functions na may Python, C# .NET o Node/TypeScript.

Nagbibigay ang mga Sample ng kumpletong solusyon na nagpapahintulot sa mga developer na:

- Bumuo at patakbuhin nang lokal: Mag-develop at mag-debug ng MCP server sa lokal na makina
- Mag-deploy sa Azure: Madaling mag-deploy sa cloud gamit ang simpleng azd up command
- Kumonekta mula sa mga client: Kumonekta sa MCP server mula sa iba't ibang client kabilang ang VS Code's Copilot agent mode at ang MCP Inspector tool

### Pangunahing Mga Tampok:

- Seguridad sa disenyo: Ang MCP server ay protektado gamit ang mga susi at HTTPS
- Mga opsyon sa authentication: Sumusuporta sa OAuth gamit ang built-in auth at/o API Management
- Network isolation: Pinapayagan ang network isolation gamit ang Azure Virtual Networks (VNET)
- Serverless architecture: Ginagamit ang Azure Functions para sa scalable, event-driven na pagpapatupad
- Lokal na pag-develop: Komprehensibong suporta para sa lokal na pag-develop at debugging
- Simpleng deployment: Pinadaling proseso ng pag-deploy sa Azure

Kasama sa repository ang lahat ng kinakailangang configuration files, source code, at infrastructure definitions para mabilis kang makapagsimula sa production-ready na pagpapatupad ng MCP server.

- [Azure Remote MCP Functions Python](https://github.com/Azure-Samples/remote-mcp-functions-python) - Sample na pagpapatupad ng MCP gamit ang Azure Functions na may Python

- [Azure Remote MCP Functions .NET](https://github.com/Azure-Samples/remote-mcp-functions-dotnet) - Sample na pagpapatupad ng MCP gamit ang Azure Functions na may C# .NET

- [Azure Remote MCP Functions Node/Typescript](https://github.com/Azure-Samples/remote-mcp-functions-typescript) - Sample na pagpapatupad ng MCP gamit ang Azure Functions na may Node/TypeScript.

## Mahahalagang Punto

- Nagbibigay ang MCP SDKs ng mga language-specific na kasangkapan para sa matibay na pagpapatupad ng MCP solutions
- Mahalaga ang proseso ng pag-debug at pagsubok para sa maaasahang mga MCP application
- Pinapayagan ng mga reusable prompt template ang consistent na interaksyon sa AI
- Ang maayos na disenyo ng workflow ay makakapag-orchestrate ng mga komplikadong gawain gamit ang maraming tools
- Kinakailangan ang pagsasaalang-alang sa seguridad, performance, at error handling sa pagpapatupad ng MCP solutions

## Ehersisyo

Magdisenyo ng praktikal na MCP workflow na tumutugon sa isang totoong problema sa iyong larangan:

1. Tukuyin ang 3-4 na tools na magiging kapaki-pakinabang sa paglutas ng problemang ito
2. Gumawa ng workflow diagram na nagpapakita kung paano nag-iinteract ang mga tools na ito
3. Ipatupad ang isang basic na bersyon ng isa sa mga tools gamit ang iyong preferred na wika
4. Gumawa ng prompt template na makakatulong sa model na epektibong gamitin ang iyong tool

## Karagdagang Resources


---

Susunod: [Advanced Topics](../05-AdvancedTopics/README.md)

**Pahayag ng Pagsuway**:  
Ang dokumentong ito ay isinalin gamit ang AI translation service na [Co-op Translator](https://github.com/Azure/co-op-translator). Bagamat nagsusumikap kami para sa katumpakan, pakatandaan na ang mga awtomatikong salin ay maaaring maglaman ng mga pagkakamali o di-tumpak na impormasyon. Ang orihinal na dokumento sa orihinal nitong wika ang dapat ituring na opisyal na sanggunian. Para sa mahahalagang impormasyon, inirerekomenda ang propesyonal na pagsasalin ng tao. Hindi kami mananagot sa anumang hindi pagkakaunawaan o maling interpretasyon na maaaring magmula sa paggamit ng salin na ito.