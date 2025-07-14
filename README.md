
# 🧠 LLM Training Journey (jul–dic 2025)

Este repositorio documenta mi camino para aprender a crear, entrenar y desplegar un modelo de lenguaje grande (LLM) desde cero antes de diciembre de 2025. A continuación, encontrarás el cronograma detallado por semanas, incluyendo teoría, práctica, recursos y entregables.

---

## 🔹 Semana 0 (8–14 jul): Orientación & base moderna de Transformers
**Recursos**:
- [Hugging Face LLM Course – Track Scientist](https://huggingface.co/blog/mlabonne/llm-course)
- [Attention Is All You Need (paper)](https://arxiv.org/abs/1706.03762)

**Actividades**:
- Repaso opcional: Python avanzado, PyTorch.
- Completar lecciones 1–3 del LLM Course.
- Implementar un encoder Transformer básico.

**Entregable**: Notebook con self-attention + curvas de pérdida.

---

## 🔹 Semana 1 (15–21 jul): nanoGPT & Scaling Laws
**Recursos**:
- [Let’s Build GPT – Andrej Karpathy (video)](https://youtu.be/kCc8FmEb1nY)
- [nanoGPT (repo)](https://github.com/karpathy/nanoGPT)
- [Scaling Laws for LMs (paper)](https://arxiv.org/abs/2001.08361)

**Actividades**:
- Clonar nanoGPT, explorar el código.
- Entrenar modelo de 6M parámetros.
- Resumir 3 hallazgos de escalamiento.

**Entregable**: Script + informe de resultados.

---

## 🔹 Semana 2 (22–28 jul): Construcción de corpus limpio
**Recursos**:
- [trafilatura (scraping)](https://github.com/adbar/trafilatura)
- [datasketch (MinHash)](https://ekzhu.github.io/datasketch/)
- [fastText (lang-id)](https://fasttext.cc/)

**Actividades**:
- Scraping y limpieza de texto gubernamental.
- Filtrado de idioma y deduplicación.
- Guardado final en Parquet.

**Entregable**: Corpus limpio con métricas.

---

## 🔹 Semana 3 (29 jul – 4 ago): Tokenización personalizada
**Recursos**:
- [HF Tokenizers Course](https://huggingface.co/learn/nlp-course/chapter6/6)
- [tokenizers API](https://github.com/huggingface/tokenizers)

**Actividades**:
- Entrenar tokenizer BPE (50k).
- Medir coverage y publicar en HF Hub.

**Entregable**: Tokenizer entrenado + análisis.

---

## 🔹 Semana 4 (5–11 ago): Arquitectura GPT (“MiniGPT”)
**Recursos**:
- [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/)
- [FlashAttention-3](https://github.com/Dao-AILab/flash-attention)

**Actividades**:
- Codificar bloques GPT en PyTorch.
- Integrar FlashAttention.
- Validar con pruebas unitarias.

**Entregable**: Módulo MiniGPT documentado.

---

## 🔹 Semana 5 (12–18 ago): Entrenamiento inicial (125M)
**Recursos**:
- [HF Efficient Transformers](https://huggingface.co/blog/efficient-transformers)
- [Weights & Biases](https://wandb.ai/)

**Actividades**:
- Configurar entrenamiento con FlashAttention y Lightning.
- Monitorear entrenamiento.

**Entregable**: Modelo 125M entrenado + dashboard de métricas.

---

## 🔹 Semana 6–7 (19 ago – 1 sep): Modelo 350–700M con FSDP
**Recursos**:
- [FSDP Tutorial PyTorch](https://docs.pytorch.org/tutorials/intermediate/FSDP_tutorial.html)

**Actividades**:
- Implementar y probar FSDP.
- Entrenar modelo completo 350M.

**Entregable**: Modelo entrenado + curvas.

---

## 🔹 Semana 8–9 (2–15 sep): Fine-tuning PEFT (LoRA)
**Recursos**:
- [PEFT Docs – HF](https://huggingface.co/docs/peft/index)

**Actividades**:
- Preparar dataset conversacional.
- Afinar con LoRA.

**Entregable**: Modelo LoRA afinado + métricas.

---

## 🔹 Semana 10 (16–22 sep): Alineación con DPO
**Recursos**:
- [DPO paper](https://arxiv.org/abs/2305.18290)
- [TRL library](https://github.com/huggingface/trl)

**Actividades**:
- Extraer pares de preferencias.
- Aplicar DPO.

**Entregable**: Modelo alineado + comparación.

---

## 🔹 Semana 11–12 (23 sep – 6 oct): Quantización y Serving
**Recursos**:
- [llama.cpp (GGUF)](https://github.com/ggerganov/llama.cpp)
- [vLLM](https://vllm.ai)

**Actividades**:
- Cuantizar modelo y evaluar pérdida.
- Servir en vLLM con latencia <200 ms.

**Entregable**: Modelo listo para producción.

---

## 🔹 Semana 13–15 (7–27 oct): Escalado en la nube (1–3B)
**Recursos**:
- [DeepSpeed ZeRO-3](https://deepspeed.ai/tutorials/zero/)

**Actividades**:
- Configurar entorno A100 (LambdaLabs).
- Entrenar modelo 1.3B completo.

**Entregable**: Checkpoint + logs + evaluación.

---

## 🔹 Semana 16–17 (28 oct – 10 nov): Federated (opcional)
**Recursos**:
- [Flower](https://flower.ai)
- [Photon](https://github.com/epfml/photon)

**Actividades**:
- Prueba de entrenamiento federado.

**Entregable**: Miniinforme técnico.

---

## 🔹 Semana 18–19 (11–24 nov): Evaluación
**Recursos**:
- [RAGAS](https://github.com/explodinggradients/ragas)
- [HELM](https://crfm.stanford.edu/helm/latest/)

**Actividades**:
- Evaluar con RAGAS y HELM.

**Entregable**: Comparativa de desempeño vs GPTs.

---

## 🔹 Semana 20–22 (25 nov – 15 dic): Integración
**Actividades**:
- Integrar modelo en microservicio `ms-chats`.
- Simular uso concurrente y analizar.

**Entregable**: Demo funcional en entorno real.

---

## 🔹 Semana 23–25 (16–29 dic): Documentación y entrega final
**Actividades**:
- Escribir white-paper.
- Grabar video demo.
- Preparar presentación final.

**Entregable**: Paquete de entrega final documentado.

---

## ✅ Repaso opcional (no se elimina, se refuerza si es necesario)
- Python avanzado, PEP-8, PyTorch
- Docker, Git, entornos venv
- Visión computacional (YOLO, OCR)
- LangChain, LangGraph, RAG y SQL (tus agentes)

---

Este plan es intensivo (6–7 h diarias), progresivo y está diseñado para que puedas crear y entrenar un LLM desde cero en un entorno real.

¡Vamos con todo!
