참고: https://github.com/awslabs/llm-hosting-container/blob/main/examples/huggingface/huggingface-large-model-inference.ipynb

- Huggingface Model
  - https://huggingface.co/meta-llama/Llama-2-7b-chat-hf
  - sagemaker code: 오른쪽 비행기 dropdown -> amazon sagemaker

local host에서 실행할 경우 ~/.aws/config에 아래와 같이 Role 추가
IAM User 가 Role 권한을 위임 받을 수 있도록 Assume Role 사전에 설정이 되어 있어야 한다.

[default]
role_arn = arn:aws:iam::532805286864:role/AdminRole
source_profile = default
region = ap-northeast-2

위 AdminRole은 SageMakerExecutionRole의 principal
- AmazonSageMakerFullAccess Policy를 반드시 가지고 있어야 함.