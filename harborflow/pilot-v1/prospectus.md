---
schema_version: "1.0.0"
title: "HarborFlow Devnet Pilot Series"
summary: "A small HarborFlow pilot offering used to prove the Yieldia lifecycle on Solana devnet."
prospectus_id: "harborflow-pilot-v1"
prospectus_id_hash: "sha256:Eb4gy1by917TLAc7B2c2wjzeBz8jXZLguFbjohTnn1At"
issuer_account: "BFaJTiS9z8sgHS2ewvRPoTLLSXUrPBEGxtdqSRNWNagL"
issuer_name: "HarborFlow"
document_uri: "https://raw.githubusercontent.com/yieldia-labs/devnet-data/main/harborflow/pilot-v1/prospectus.md"
proof_pack_uri: "https://raw.githubusercontent.com/yieldia-labs/devnet-data/main/harborflow/pilot-v1/proof-pack.json"
proof_pack_hash: "sha256:2YbjQkmscvXU19PKq65gE93TcLreG9VkySN99v7gS2i8"
terms_hash: "sha256:4PkMbxfmZi9HrJ22KySTsQNWYRbB4PiV4d1QjSuT5Bvf"

terms:
  token_issuance_amount: "100"
  token_unit_price: "1000000"
  token_price_asset: "6To6oV5uLtZCTXg7kD6cSnKqsN6UWxjkEAZnDsWF81WM"
  issuer_treasury: "D4b8MtxYQNyLns4cCTw96rkvhUS2nJEvR7pWcrkNAZw2"
  yield_asset: "6To6oV5uLtZCTXg7kD6cSnKqsN6UWxjkEAZnDsWF81WM"
  claim_window: "3024000"
  sale_window: "3024000"
  settle_window: "3024000"
---

# HarborFlow Devnet Pilot Series Prospectus

This is fictional test data for the Yieldia devnet proof. It is not an investment offer and has no real-world claim.

## 1. Prospectus Provenance

- Issuer: `HarborFlow` (`BFaJTiS9z8sgHS2ewvRPoTLLSXUrPBEGxtdqSRNWNagL`)
- Authorized author: `DQxiJX4b8xFMEpJTG6TUbymU8CTbBzGhR584CnH7NcXn`
- Prospectus ID: `harborflow-pilot-v1`
- Canonical document and proof-pack locations are declared in the frontmatter.

## 2. Offering Summary

The series proves the successful path from Greenlight approval through a sold-out primary sale, settlement, allocation
claims, Yield funding, redemption, and offering close. Two devnet buyers are expected to purchase 50 units each.

## 3. Issuer Context

HarborFlow is a fictional Solana-native treasury automation protocol. Its devnet authority controls the onchain Issuer
account and the YTUSD treasury token account used to receive primary-sale proceeds.

## 4. Core Terms

- Capital instrument: `HarborFlow Devnet Pilot Series` (`HFLOW-P1`)
- Fixed issuance: `100` whole instrument tokens
- Unit price: `1 YTUSD` (`1,000,000` base units; YTUSD has 6 decimals)
- Gross primary proceeds: `100 YTUSD`
- Price and Yield asset: YTUSD mint `6To6oV5uLtZCTXg7kD6cSnKqsN6UWxjkEAZnDsWF81WM`
- Proceeds destination: `D4b8MtxYQNyLns4cCTw96rkvhUS2nJEvR7pWcrkNAZw2`
- Sale window: `3,024,000` slots (approximately one week at 200 ms per slot)
- Settle window: `3,024,000` slots after the sale deadline (approximately one week at 200 ms per slot)
- Claim window: `3,024,000` slots after Yield funding (approximately one week at 200 ms per slot)

Slot counts are authoritative; wall-clock durations are estimates. At a 400 ms slot target, each window lasts
approximately two weeks. A sold-out offering may settle immediately. The offering may close before the claim deadline
once every instrument token has been redeemed.

## 5. Economic Claim

After successful primary settlement, HarborFlow intends to fund the Yield vault with `110 YTUSD`. Each of the 100
instrument tokens then redeems for `1.10 YTUSD` when every token is redeemed. The onchain payout is determined by the
actual funded vault amount and the program's integer pro-rata calculation.

The revenue period runs from `2026-08-15` through `2026-09-15`; the target payment date is `2026-09-30`. No conversion
into a later series is promised. If the Yield vault is not funded, holders have no redemption path until funding occurs.

## 6. Source Of Funds

The planned source is test YTUSD allocated by the Yieldia devnet operator to HarborFlow. The operator controls the
devnet YTUSD mint and can supply the issuer with the additional amount required beyond primary-sale proceeds.

## 7. Evidence Pack

The accompanying proof pack identifies the issuer, author, YTUSD mint, treasury account, canonical document location,
and relevant devnet Explorer references. All operating and economic claims are synthetic test assertions.

## 8. Risks

- Devnet may be reset, congested, rate-limited, or unavailable.
- YTUSD has no real-world value and is controlled by a test operator.
- The test may fail if buyers do not purchase all 100 units or if the issuer does not settle and fund Yield.
- Classic SPL instrument tokens are transferable after allocation; after offering close, unredeemed tokens are inert
  but may still remain in token accounts.

## 9. Market Readiness

Participation is open to controlled devnet wallets. No compliance, liquidity, valuation, or production-readiness claim
is made. The series exists only to exercise observable program state and participant transactions end to end.

## 10. Supporting Materials

- Issuer metadata: `https://raw.githubusercontent.com/yieldia-labs/devnet-data/main/harborflow/issuer.json`
- YTUSD mint: `https://explorer.solana.com/address/6To6oV5uLtZCTXg7kD6cSnKqsN6UWxjkEAZnDsWF81WM?cluster=devnet`
- Intended use of proceeds: devnet lifecycle testing only
- Prepared: `2026-08-12`
