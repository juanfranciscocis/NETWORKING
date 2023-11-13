# study-guide:-computer-networking-chapter-2


###-required-reading
sections:-2.1,-2.2,-2.4,-2.5,-2.6-and-2.7-

##-technology-perspective

1.-what-are-the-different-technologies-used-for-connecting-nodes-in-a-computer-network?

the-different-technologies-used-for-connecting-nodes-in-a-computer-network-are:
---copper-based-technologies:
-----dsl-(digital-subscriber-line):-utilizes-twisted-pair-copper-wires-for-last-mile-connections,-providing-up-to-100-mbps-bandwidth.-
-----g.fast:-a-copper-based-technology-often-used-within-multi-dwelling-apartment-buildings,-offering-up-to-1-gbps-bandwidth.
---fiber-optic-technology:
-----pon-(passive-optical-network):-uses-optical-fiber-for-high-speed-connections,-offering-up-to-10-gbps-bandwidth.-commonly-used-for-connecting-homes-and-businesses.
---mobile-or-cellular-networks:
-----4g-(evolving-into-5g):-connects-mobile-devices-to-the-internet-and-can-serve-as-an-internet-connection-for-homes-and-offices.-offers-mobility-while-maintaining-internet-connectivity.
---backbone-links:
-----modern-backbone-links-primarily-use-fiber-optics-and-a-technology-called-sonet-(synchronous-optical-network)-for-high-speed,-long-distance-connections-between-cities.-originally-developed-for-telephone-carriers.
---local-area-networks-(lans):
-----ethernet-and-wi-fi:-dominant-technologies-used-for-connecting-devices-within-a-building-or-campus.-ethernet-uses-wired-connections,-while-wi-fi-provides-wireless-connectivity.


##-encoding

1.-what-is-encoding-in-the-context-of-computer-networking?

is-the-process-of-converting-binary-data-(comprising-1s-and-0s)-into-signals-that-can-be-transmitted-over-physical-links-in-a-network.-encoding-is-essential-to-ensure-that-the-binary-data-from-a-source-node-can-be-effectively-transmitted-to-a-destination-node-through-the-network's-communication-channels.

2.-explain-the-difference-between-analog-and-digital-signals.

--analog-signals:
----analog-signals-are-continuous-waveforms-that-can-take-on-a-range-of-values-within-a-given-range.
----these-signals-represent-data-as-continuously-varying-voltage-levels,-frequencies,-or-amplitudes.
----analog-signals-are-typically-used-in-analog-communication-systems,-such-as-traditional-voice-calls-over-landline-phones.
----they-are-susceptible-to-signal-degradation-over-long-distances-and-are-more-sensitive-to-external-interference.
--digital-signals:
----digital-signals-are-discrete-and-represent-data-as-a-series-of-binary-values,-typically-1s-and-0s.
----these-signals-have-distinct-levels,-such-as-high-and-low-voltage-states-or-on-and-off-states.
----digital-signals-are-used-in-digital-communication-systems,-such-as-computer-networks-and-the-transmission-of-digital-data.
----they-are-less-susceptible-to-signal-degradation-over-long-distances-and-are-more-resilient-to-noise-and-interference.


3.-explain-the-different-types-of-encoding-used-in-computer-networks

--non-return-to-zero-(nrz)-encoding:
-----nrz-encoding-is-a-simple-binary-encoding-scheme.
-----it-maps-the-binary-value-1-onto-the-high-signal-and-the-binary-value-0-onto-the-low-signal.
-----the-drawback-of-nrz-is-that-it-can-lead-to-long-sequences-of-consecutive-1s-or-0s,-causing-issues-like-baseline-wander,-where-the-receiver's-ability-to-distinguish-between-low-and-high-signals-is-compromised-due-to-long-signal-durations.

--non-return-to-zero-inverted-(nrzi)-encoding:
----nrzi-is-an-encoding-scheme-that-addresses-the-issue-of-consecutive-1s-in-nrz-encoding.
----in-nrzi,-a-transition-from-the-current-signal-level-encodes-a-1,-while-staying-at-the-current-signal-level-encodes-a-0.
----nrzi-helps-prevent-consecutive-1s-from-causing-problems-with-baseline-wander.

--manchester-encoding:
-----manchester-encoding-is-an-encoding-scheme-that-combines-the-clock-signal-with-data-signal.
-----it-encodes-0-as-a-low-to-high-transition-and-1-as-a-high-to-low-transition.
-----manchester-encoding-ensures-frequent-signal-transitions,-aiding-clock-recovery,-but-it-doubles-the-transition-rate,-reducing-efficiency.
-----it-helps-the-receiver-maintain-synchronization-with-the-sender's-clock,-critical-for-accurate-data-decoding.

--4b/5b-encoding:
----4b/5b-encoding-aims-to-balance-efficiency-and-signal-transitions.
----it-inserts-extra-bits-into-the-data-stream-to-break-up-long-sequences-of-0s-or-1s.
----every-4-bits-of-actual-data-are-encoded-into-a-5-bit-code,-ensuring-that-no-more-than-three-consecutive-0s-or-1s-are-transmitted-in-a-row.
----4b/5b-encoding-achieves-80%-efficiency-while-addressing-the-problems-of-long-signal-durations-and-clock-drift.

##-error-detection

1.-what-is-error-detection-and-why-is-it-important-in-computer-networks?

error-detection-is-the-process-of-identifying-errors-or-corruption-in-data-transmitted-over-a-computer-network.-it-is-crucial-in-computer-networks-because-data-can-be-susceptible-to-various-forms-of-corruption-during-transmission-due-to-factors-like-electrical-interference,-noise,-or-other-forms-of-distortion.-detecting-errors-is-essential-to-ensure-the-integrity-and-reliability-of-data

2.-explain-the-concept-of-parity-checking-for-error-detection.

it-involves-adding-an-additional-bit,-known-as-a-parity-bit,-to-a-block-of-data.-the-parity-bit-is-chosen-so-that-the-total-number-of-1s-in-the-data-block,-including-the-parity-bit,-is-either-even-or-odd.-there-are-two-types-of-parity-checking:

--even-parity:-the-total-number-of-1s,-including-the-parity-bit,-is-made-even.
--odd-parity:-the-total-number-of-1s,-including-the-parity-bit,-is-made-odd.-

during-data-transmission,-if-an-error-occurs-and-the-number-of-1s-in-the-received-data-block-(including-the-parity-bit)-does-not-match-the-expected-parity-(even-or-odd),-an-error-is-detected.

3.-discuss-the-advantages-and-limitations-of-parity-checking.


advantages-of-parity-checking:
--simplicity:-parity-checking-is-straightforward-to-implement-and-requires-minimal-additional-overhead.
--basic-error-detection:-it-can-detect-single-bit-errors-effectively.

limitations-of-parity-checking:
--limited-error-detection:-parity-checking-can-only-detect-errors;-it-cannot-correct-them.
--limited-to-single-bit-errors:-it-is-only-effective-at-detecting-single-bit-errors,-making-it-inadequate-for-detecting-multiple-or-more-complex-errors.
--inefficiency:-it-is-not-very-efficient-for-detecting-errors-in-large-data-blocks-or-over-noisy-channels.

4.-describe-the-process-of-using-checksums-for-error-detection.

the-process-of-using-checksums-for-error-detection-are:
--1.-the-sender-calculates-the-checksum-value-based-on-the-data.
--2.-the-sender-appends-or-includes-the-checksum-in-the-transmitted-data.
--3.-the-receiver-calculates-its-own-checksum-based-on-the-received-data.
--4.-the-receiver-compares-the-calculated-checksum-with-the-received-checksum.
--5.-if-they-match,-the-data-is-assumed-to-be-error-free;-if-not,-an-error-is-detected.

5.-explain-cyclic-redundancy-checks.-

it-uses-polynomial-division-to-generate-a-redundancy-check-value-(crc-value)-that-is-appended-to-the-data-before-transmission.-the-receiver-performs-the-same-polynomial-division-on-the-received-data-and-checks-whether-the-calculated-crc-value-matches-the-received-crc-value.

##-reliable-transmission

1.-what-is-reliable-transmission-and-why-is-it-important-in-computer-networks?

is-the-ability-of-a-network-protocol-to-ensure-that-data-sent-from-one-node-to-another-arrives-correctly-and-in-the-right-order,-without-errors-or-omissions

2.-explain-the-concept-of-stop-and-wait-protocol-for-reliable-transmission.

in-this-protocol,-after-sending-a-data-frame,-the-sender-waits-for-an-acknowledgment-(ack)-from-the-receiver.-if-the-sender-does-not-receive-an-ack-within-a-reasonable-time-(timeout),-it-assumes-that-the-frame-was-lost-or-corrupted-and-retransmits-it.-the-receiver-acknowledges-the-successful-receipt-of-each-frame.

3.-discuss-the-advantages-and-limitations-of-stop-and-wait-protocol.

--advantages-of-the-stop-and-wait-protocol:
----simplicity:-it-is-easy-to-understand-and-implement.
----error-detection:-the-sender-can-detect-lost-or-corrupted-frames-and-retransmit-them.
----flow-control:-it-naturally-provides-a-form-of-flow-control-since-the-sender-waits-for-acks-before-sending-more-data.
--limitations-of-the-stop-and-wait-protocol:
----inefficiency:-it-has-low-efficiency,-especially-on-high-latency-links,-because-the-sender-can-have-only-one-frame-in-transit-at-a-time.
----limited-throughput:-the-protocol-does-not-fully-utilize-the-available-bandwidth,-leading-to-underutilization-of-the-network.
----high-latency:-on-high-latency-links,-the-round-trip-time-for-an-ack-can-be-significant,-causing-delays.

4.-describe-the-process-of-using-sliding-window-protocol-for-reliable-transmission.

--1.-assigning-sequence-numbers-to-each-frame-to-maintain-order.
--2.-maintaining-a-send-window-size-(sws)-that-determines-the-number-of-outstanding-frames-the-sender-can-transmit.
--3.-maintaining-a-receive-window-size-(rws)-on-the-receiver-side-to-specify-the-number-of-out-of-order-frames-the-receiver-is-willing-to-accept.
--4.-using-acknowledgments-(acks)-to-confirm-the-receipt-of-frames-and-allowing-the-sender-to-advance-its-window.
--5.-implementing-timeouts-to-trigger-frame-retransmission-in-case-of-lost-or-delayed-acks.
--6.-handling-sequence-number-wrapping-in-a-finite-sequence-number-space.


##-ethernet-and-multiple-access-networks

1.-what-is-ethernet-and-how-does-it-work?

ethernet-is-a-local-area-networking-technology-where-multiple-devices-are-connected-to-a-shared-communication-medium,-typically-using-twisted-copper-pairs-or-optical-fibers.-each-device-has-a-unique-ethernet-address-(mac-address),-and-they-communicate-by-sending-frames-over-the-network.

2.-explain-the-concept-of-multiple-access-networks.

multiple-access-networks-allow-multiple-devices-(nodes)-to-transmit-and-receive-data-over-a-shared-communication-medium.-nodes-need-to-follow-certain-protocols-to-access-the-shared-medium-fairly-and-avoid-collisions.

3.-discuss-the-advantages-and-limitations-of-ethernet.

--advantages:
------simplicity:-ethernet-is-easy-to-set-up-and-administer.
------cost-effective:-it-uses-inexpensive-cables-and-network-adaptors.
------backward-compatibility:-newer-ethernet-versions-are-backward-compatible-with-older-ones.
------reliable:-collision-detection-and-retransmission-mechanisms-enhance-reliability.
--limitations:
------limited-distance:-ethernet-has-a-maximum-cable-length,-typically-around-100-meters-for-twisted-pair-cables.
------limited-scalability:-in-large-networks,-collision-domains-can-become-a-limitation.-
------half-duplex-communication:-traditional-ethernet-operates-in-half-duplex-mode,-allowing-either-sending-or-receiving-at-a-time.


4.-describe-the-process-of-collision-detection-in-ethernet.

ethernet-uses-a-collision-detection-mechanism-where-each-transmitting-node-listens-while-it-sends-data.-if-it-detects-a-collision,-it-immediately-stops-transmitting,-sends-a-jamming-signal,-and-enters-a-backoff-period-during-which-it-waits-for-a-random-amount-of-time-before-attempting-to-transmit-again.

5.-give-examples-of-different-multiple-access-techniques-used-in-computer-networks.

csma/cd-(used-in-ethernet),-csma/ca-(used-in-wi-fi-networks),-time-division-multiple-access-(tdma),-frequency-division-multiple-access-(fdma),-and-code-division-multiple-access-(cdma).

##-wireless-networks

1.-what-are-wireless-networks-and-how-do-they-work?

wireless-networks-are-communication-systems-that-use-radio-waves-or-other-wireless-technologies-to-connect-devices-and-allow-them-to-exchange-data-without-the-need-for-physical-cables.-in-wireless-networks,-information-is-transmitted-over-the-air-through-electromagnetic-signals.-devices-in-a-wireless-network-communicate-using-wireless-network-adapters,-which-include-components-like-antennas-and-radios-to-send-and-receive-data-wirelessly.

2.-explain-the-concept-of-wireless-communication-channels.

wireless-communication-channels-are-pathways-through-which-wireless-signals-propagate-between-devices.-these-channels-involve-the-transmission-and-reception-of-electromagnetic-waves,-typically-in-the-radio-frequency-(rf)-spectrum.

3.-discuss-the-advantages-and-limitations-of-wireless-networks.

--advantages-of-wireless-networks:
----mobility:-wireless-networks-allow-devices-to-connect-and-communicate-while-on-the-move,-providing-flexibility-and-convenience.
-----easy-deployment:-setting-up-wireless-networks-is-often-simpler-and-more-cost-effective-than-running-physical-cables.
-----scalability:-wireless-networks-can-be-easily-expanded-by-adding-more-access-points-or-devices.
-----accessibility:-wireless-networks-provide-connectivity-in-areas-where-laying-cables-is-impractical.
-----reduced-clutter:-eliminating-cables-reduces-physical-clutter-and-simplifies-network-management.
--limitations-of-wireless-networks:
----interference:-wireless-networks-can-be-susceptible-to-interference-from-other-wireless-devices-and-obstacles-in-the-environment.
----limited-range:-wireless-signals-have-a-finite-range,-and-signal-strength-decreases-with-distance-from-the-access-point.
----security-concerns:-wireless-networks-may-be-vulnerable-to-unauthorized-access-if-not-properly-secured.
----slower-speeds:-wireless-networks-can-have-lower-data-transfer-rates-compared-to-wired-networks.
----reliability:-wireless-connections-can-be-less-reliable-than-wired-connections-due-to-signal-disruptions.

4.-describe-the-process-of-wireless-signal-propagation-and-interference

--signal-propagation:
----signal-propagation-is-the-process-by-which-wireless-signals-travel-from-a-transmitter-to-a-receiver.
----wireless-signals-propagate-through-the-air-as-electromagnetic-waves,-typically-in-the-radio-frequency-(rf)-spectrum.
----the-strength-of-a-wireless-signal-decreases-with-distance-from-the-transmitter,-and-it-can-be-affected-by-obstacles-in-the-environment.
--signal-interference:
----signal-interference-is-the-disruption-of-wireless-signals-by-other-wireless-devices-or-obstacles-in-the-environment.
----interference-can-cause-signal-degradation,-resulting-in-lower-signal-strength-and-reduced-data-transfer-rates.
----interference-can-be-caused-by-other-wireless-devices-operating-in-the-same-frequency-band-or-by-physical-obstacles-like-walls-or-buildings


5.-give-examples-of-different-wireless-networking-technologies-used-in-computer-networks.

--wi-fi:-a-wireless-networking-technology-that-uses-radio-waves-to-provide-wireless-connectivity-to-devices.
--bluetooth:-a-wireless-technology-that-uses-radio-waves-to-connect-devices-over-short-distances.
--cellular-networks:-wireless-networks-that-provide-mobile-connectivity-to-devices-over-large-geographical-areas.
--zigbee:-a-wireless-technology-that-uses-radio-waves-to-connect-devices-over-short-distances.
--wireless-sensor-networks-(wsns):-wireless-networks-that-use-sensors-to-collect-data-from-the-environment-and-transmit-it-wirelessly.

##-exercises

1.-show-the-manchester,-4b/5b-encoding,-and-the-resulting-nrzi-signal,-for-the
following-bit-sequence:
1110-0101-0000-0011

--manchester-encoding:

----1-is-represented-as-a-high-to-low-transition.
----0-is-represented-as-a-low-to-high-transition.

------1010-1010-0101-0101

--4b/5b-encoding:
----1110-maps-to-10010
----0101-maps-to-11001
----0000-maps-to-11110
----0011-maps-to-01100
------10010-11001-11110-01100

--nrzi-encoding:
----1-is-represented-as-a-transition-from-the-current-signal-level.
----0-is-represented-as-no-transition-from-the-current-signal-level.
------1011-0111-0000-0010

2.-show-the-manchester,-4b/5b-encoding,-and-the-resulting-nrzi-signal,-for-the
following-bit-sequence:
1101-1110-1010-1101-1011-1110-1110-1111



--manchester-encoding:

----1-is-represented-as-a-high-to-low-transition.
----0-is-represented-as-a-low-to-high-transition.

------0110-1001-0101-0110-0100-1001-1001-1000


--4b/5b-encoding:
----1101-maps-to-10010
----1110-maps-to-10101
----1010-maps-to-01011
----1101-maps-to-10010
----1011-maps-to-01010
----1110-maps-to-10101
----1110-maps-to-10101
----1111-maps-to-10110
------10010-10101-01011-10010-01010-10101-10101-10110



--nrzi-encoding:
----1-is-represented-as-a-transition-from-the-current-signal-level.
----0-is-represented-as-no-transition-from-the-current-signal-level.
------0100-0111-0100-0011-0010-0110-0010-0001





3.-suppose-we-want-to-transmit-the-message-"1011-0010-0100-1011"-and-protect-it-from-errors-using-the-crc8-polynomial-$x^8-+-x^2-+-x^1-+-1$.

--use-polynomial-long-division-to-determine-the-message-that-should-be-transmitted.
--suppose-the-leftmost-bit-of-the-message-is-inverted-due-to-noise-on-the-transmission-link.-what-is-the-result-of-the-receiver’s-crc-calculation?-how-does-the-receiver-know-that-an-error-has-occurred?

###-polynomial-long-division-for-crc-calculation

**message:**-1011-0010-0100-1011
**crc8-polynomial:**-\(x^8-+-x^2-+-x-+-1\)

1.-**polynomial-long-division:**

```
----------------101101001000101100000000--(message-with-zeros)
------------------------------------
x^8-+-x^2-+-x-+-1-|-1011001000101100000000
----------------1011001000101100000000
--------------------
----------------------------0-0000000000
```

**result:**-the-remainder-is-0,-indicating-no-error.-the-message-to-be-transmitted-is:-1011-0010-0100-1011-00000000

###-simulated-inverted-leftmost-bit

**original-message:**-1011-0010-0100-1011-00000000
**inverted-leftmost-bit:**-0011-0010-0100-1011-00000000

2.-**crc-calculation-with-inverted-leftmost-bit:**

```
----------------101101001000101100000000--(crc8-polynomial)
------------------------------------
x^8-+-x^2-+-x-+-1-|-0011001000101100000000
----------------1011001000101100000000
--------------------
----------------------------0-0000000000
```

**result:**-the-remainder-is-0,-which-means-no-error-is-detected.-however,-the-receiver-does-not-know-that-an-error-has-occurred.





4.-consider-an-arq-protocol-that-uses-only-negative-acknowledgments-(naks),-but-no-positive-acknowledgments-(acks).-describe-what-timeouts-would-have-to-be-scheduled.-explain-why-an-ack-based-protocol-is-usually-preferred-to-a-nak-based-protocol.

in-a-negative-acknowledgment-(nak)-only-arq-protocol:

--1.-timeout-for-initial-transmission:-sender-starts-a-timer-when-transmitting-data.-if-no-nak-is-received-within-the-timeout,-it-assumes-success.

--2.-timeout-for-nak-reception:-after-receiving-a-nak,-the-sender-retries-and-starts-a-timer.-if-no-response-(ack-or-nak)-is-received-within-the-timeout,-it-assumes-success.

--3.-limited-retransmissions:-a-maximum-retry-limit-is-set.-if-reached-without-acknowledgment,-the-frame-is-considered-lost.

--4.-exponential-backoff:-timeout-duration-may-increase-after-each-retransmission-to-reduce-collisions.

ack-based-protocols-are-preferred-due-to-higher-reliability,-efficiency,-and-reduced-network-traffic.-acks-confirm-successful-reception,-while-naks-introduce-uncertainties-and-additional-overhead.

5.-draw-a-timeline-diagram-for-the-sliding-window-algorithm-with-sws-=-rws-=-3-frames,-for-the-following-two-situations.-use-a-timeout-interval-of-about-2-×-rtt.

--frame-4-is-lost.
--frames-4-to-6-are-lost.

certainly,-here-are-the-timeline-diagrams-for-the-sliding-window-algorithm-with-sws-=-rws-=-3-frames,-using-"-"-to-represent-blank-spaces-in-the-tables:

###-situation-1:-frame-4-is-lost

sender's-perspective:

|---|---|---|-4-|-5-|-6-|---|---|---|---|---|---|
|---|---|---|---|---|---|---|---|---|---|---|---|
|-s1-|-s2-|-s3-|-s4-|-s5-|-s6-|---|---|---|---|---|---|

receiver's-perspective:

|---|---|---|-4-|-5-|-6-|---|---|---|---|---|---|
|---|---|---|---|---|---|---|---|---|---|---|---|
|---|---|---|---|---|---|-r1-|-r2-|-r3-|-r4-|-r5-|-r6-|

###-situation-2:-frames-4-to-6-are-lost

sender's-perspective:

|---|---|---|-4-|-5-|-6-|---|---|---|---|---|---|
|---|---|---|---|---|---|---|---|---|---|---|---|
|-s1-|-s2-|-s3-|-s4-|-s5-|-s6-|---|---|---|---|---|---|

receiver's-perspective:

|---|---|---|-4-|-5-|-6-|---|---|---|---|---|---|
|---|---|---|---|---|---|---|---|---|---|---|---|
|---|---|---|-r1-|-r2-|-r3-|-r4-|-r5-|-r6-|---|---|---|
