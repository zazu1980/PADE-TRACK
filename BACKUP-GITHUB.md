# Backup automático no GitHub

No fim de cada jogo a app guarda duas cópias num repositório **privado** teu:
- `padel-track-backup.json` — backup completo (serve para repor os dados)
- `acoes.csv` — uma linha por ação (abre no Excel ou Google Sheets)

Cada gravação fica no histórico de versões do GitHub, por isso podes voltar atrás.

## Passo 1 — Criar o repositório privado (no computador)
1. Vai a https://github.com/new
2. Nome: `padel-dados`
3. Escolhe **Private** (importante!)
4. Marca **Add a README file**
5. Clica **Create repository**

## Passo 2 — Criar a chave de acesso (token)
1. No GitHub, clica na tua foto (canto superior direito) → **Settings**.
2. Barra lateral, no fim: **Developer settings → Personal access tokens → Fine-grained tokens**.
3. Clica **Generate new token** e preenche:
   - **Token name:** Padel Track
   - **Expiration:** 1 year (ou o máximo permitido)
   - **Repository access:** *Only select repositories* → escolhe `padel-dados`
   - **Permissions → Repository permissions → Contents:** *Read and write*
4. Clica **Generate token** e **copia a chave** (começa por `github_pat_`). Só aparece uma vez. Envia-a para o telemóvel de forma segura (por exemplo, numa nota protegida).

## Passo 3 — Ligar na app (no telemóvel)
1. ⚙ Definições → secção **Backup**.
2. **Repositório:** `o-teu-utilizador/padel-dados`
3. **Chave de acesso:** cola o token.
4. Toca em **Guardar** (a app confirma que o repositório é privado) e depois em **Fazer backup agora**.

## Repor os dados (telemóvel novo)
1. Instala a app, vai a Definições → Backup e liga o repositório e a chave.
2. Toca em **Repor do GitHub** e confirma.

## Notas
- Sem internet no fim do jogo, fica pendente e envia-se quando a app abrir com rede.
- Usa a app com **um só telemóvel**: cada backup substitui o anterior (as versões antigas ficam no histórico do GitHub).
- A app recusa repositórios públicos, para não expor os dados dos jogadores.
- A chave só fica guardada nesse telemóvel. Se o perderes, apaga a chave em GitHub → Settings → Developer settings.
- A chave expira. Quando isso acontecer, aparece "chave inválida ou expirada": cria uma nova e cola-a na app.
