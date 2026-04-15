# ComfyUI RAG Chat Node

ComfyUI custom node for RAG-based knowledge base chat using Volcengine service API.

## Installation

1. Copy `comfyui_volcengine_rag_node.py` to ComfyUI's `custom_nodes` folder
2. Restart ComfyUI

## Nodes

### VLMConfigNode

Configure API credentials.

**Parameters**:
- `apikey`: API Key from Volcengine platform
- `service_resource_id`: Service resource ID
- `base_url`: API endpoint (default: `api-knowledgebase.mlp.cn-beijing.volces.com`)

### RAGChatNode

Send query and get response from RAG service.

**Inputs**:
- `vlm_config`: Output from VLMConfigNode
- `query`: User query text

**Output**:
- Response text from LLM

## Usage

1. Add **VLMConfigNode** and fill in credentials
2. Add **RAGChatNode** and connect the config
3. Fill in query and run
