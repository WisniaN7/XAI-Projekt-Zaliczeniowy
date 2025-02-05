
# For runpod: edit pod to have port 3000 and 100GB of temporary storage
python -m llava.serve.controller --host 0.0.0.0 --port 10000

# Open new terminal, keep previous one open
<!-- python -m llava.serve.model_worker --host 0.0.0.0 --controller http://localhost:10000 --port 40000 --worker http://localhost:40000 --model-path liuhaotian/llava-v1.5-13b -->

# Open new terminal, keep previous one open
python -m llava.serve.gradio_web_server --controller http://localhost:10000 --model-list-mode reload --port 3000

---

Linux/WSL: go to localhost:10000

RunPod: Click http service port 3000 button