module digiOTA (
    output wire Out,
    input wire Vip,
    input wire Vin
);
    wire INn, INp, CMP, EN, not_EN, Op, On;

    not IV1 (INn, Vip);
    not IV2 (CMP, INn);
    not IV3 (INp, Vin);
    not IV4 (INp, CMP); // This line seems redundant, consider reviewing this logic
    not IV5 (Op, INn);
    not IV6 (On, INp);
    not IV7 (not_EN, EN);
    xor XOR1 (EN, Op, On);
    bufif1 BT1 (Out, EN, Op);
    notif1 IT1 (CMP, not_EN, Op);

endmodule
