# Plano de Manutenção

Para garantir que o ReFeed.inc opere com a disponibilidade exigida de 99,9% (RNF03) e tempo de resposta de até 2 segundos (RNF02), as atividades de manutenção serão divididas em quatro categorias estruturadas.

## Manutenção Corretiva

Focada na correção de falhas e *bugs* reportados por usuários ou detectados pelos *logs* do sistema.

- Correção de falhas no *upload* de fotos e certificados de resíduos orgânicos (RF02) em dispositivos Android/iOS específicos
- Tratamento de exceções e quebras no fluxo de *checkout* da API de pagamentos Stripe/PIX/boleto (RF10)
- Ajustes em erros de roteirização e falhas de conexão de geolocalização no módulo de Logística (RF14 e RF15)

Acordo de Nível de Serviço (SLA) para correção de *bugs* críticos (ex: travamento de *checkout* ou falha no pagamento a fornecedores) em até 2 horas.

## Manutenção Preventiva

Atividades programadas para evitar a ocorrência de falhas futuras e garantir a integridade do ecossistema.

- Análise preventiva de vulnerabilidades e varreduras de segurança nas APIs Node.js e rotas protegidas por JWT
- Renovação de certificados SSL/TLS e revisão de regras de acesso nas permissões RBAC no banco PostgreSQL
- Testes periódicos de carga simulada (estresse) antes de épocas de safra e alta demanda, garantindo o funcionamento do *Auto-scaling* (RNF05)
- Verificação periódica da integridade dos dados de rastreabilidade no Traceability Service

## Manutenção Adaptativa

Modificações necessárias para que o sistema continue operacional diante de mudanças externas (plataformas, leis, dependências).

- Atualizações das SDKs do Expo e do React Native decorrentes de novas exigências e atualizações de segurança do iOS e Android (Google Play e App Store)
- Ajustes nas políticas de privacidade e criptografia no AWS S3 caso ocorram atualizações regulatórias na LGPD ou na Política Nacional de Resíduos Sólidos (RNF01)
- Atualizações na API de mapas de terceiros (Google Maps/Mapbox) e regras de precificação da API da Stripe
- Adequação a novas normas do CONAMA ou resoluções ambientais estaduais para destinação de resíduos orgânicos

## Manutenção Evolutiva

Implementação de novas regras de negócio e recursos que agregam valor ao ecossistema a partir do *feedback* dos usuários.

- Migração de requisitos categorizados no *backlog* do MVP como *Should Have* e *Could Have* (ex: Otimização de Rotas por IA RF15, Histórico de Rastreabilidade RF12)
- Implementação futura do marketplace de insumos agrícolas integrado e do programa de certificação orgânica digital (classificados como *Won't Have* no escopo inicial)
- Expansão do motor de rastreabilidade para rastrear o ciclo de vida completo do resíduo até o uso final pelo produtor rural
