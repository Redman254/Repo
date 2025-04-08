import React, { useState } from 'react';

const workstreams = [
  {
    title: "Autodesk Construction Cloud Building Information Modeling Foundation",
    summary: "Establishes Building Information Modeling coordination and naming standards.",
    iso: [
      "ISO 19650-1:2018 – Organization and digitization of information about buildings and civil engineering works",
      "ISO 19650-2:2018 – Delivery phase of assets"
    ],
    ai: "None",
    persona: "Building Information Modeling Coordinator ensures models align across stakeholders."
  },
  {
    title: "Autodesk Construction Cloud Asset Register",
    summary: "Defines asset hierarchies and templates.",
    iso: [
      "ISO 55000:2014 – Asset management – Overview, principles and terminology",
      "ISO 30186:2022 – Digital Twin – Maturity model and guidance for a maturity assessment"
    ],
    ai: "Machine Learning, Knowledge Graphs",
    persona: "Asset Manager tracks lifecycle and reliability."
  },
  {
    title: "Field Data Collection",
    summary: "Smart capture and validation of site data.",
    iso: [
      "ISO/IEC 5339:2024 – Guidance for Artificial Intelligence applications",
      "ISO 8000-63:2017 – Data quality – Data quality management: Product data quality"
    ],
    ai: "Computer Vision, Natural Language Processing",
    persona: "Field Engineer uses Augmented Reality and voice prompts."
  },
  {
    title: "Data Preparation",
    summary: "Prepares data schemas for Geographic Information Systems integration.",
    iso: [
      "ISO/IEC 5259-3:2024 – Data quality for analytics and machine learning – Part 3: Management guidelines",
      "ISO 25059:2024 – Systems and software Quality Requirements and Evaluation – Quality model for Artificial Intelligence systems"
    ],
    ai: "Large Language Models",
    persona: "Data Steward validates schema mappings."
  },
  {
    title: "Autodesk Construction Cloud to Environmental Systems Research Institute Transformation",
    summary: "Transforms Building Information Modeling into Geographic Information System-ready formats.",
    iso: [
      "ISO 19157:2013 – Geographic information – Data quality",
      "ISO 22301:2019 – Security and resilience – Business continuity management systems – Requirements"
    ],
    ai: "Machine Learning",
    persona: "Geographic Information System Technician synchronizes datasets for dashboards."
  },
  {
    title: "Environmental Systems Research Institute Geographic Information System Implementation",
    summary: "Establishes spatial rules and three-dimensional visuals.",
    iso: [
      "ISO 37173:2023 – Smart infrastructure – Guidance for smart building information systems",
      "ISO 37105:2019 – Smart city reference model – Guidance on smart city use cases"
    ],
    ai: "Computer Vision",
    persona: "Urban Planner simulates infrastructure change."
  },
  {
    title: "Enterprise Integration",
    summary: "Links application programming interfaces, portals and dashboards.",
    iso: [
      "ISO/IEC 42001:2023 – Artificial Intelligence Management System",
      "ISO 22313:2020 – Security and resilience – Business continuity management systems – Guidance on the use of ISO 22301"
    ],
    ai: "Machine Learning, Natural Language Processing",
    persona: "Chief Information Officer reviews live key performance indicators and telemetry."
  },
  {
    title: "Persona Use Cases",
    summary: "User stories where Artificial Intelligence accelerates delivery.",
    iso: [
      "ISO 8000-63:2017 – Data quality – Data quality management: Product data quality",
      "ISO 30186:2022 – Digital Twin – Maturity model and guidance for a maturity assessment"
    ],
    ai: "Natural Language Processing, Machine Learning, Computer Vision",
    persona: "Simulation analyst builds scenarios with Artificial Intelligence."
  }
];

export default function InteractiveWorkstreamDashboard() {
  return (
    <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 p-6">
      {workstreams.map((item, index) => (
        <div key={index} className="border rounded-xl shadow bg-white p-4 hover:shadow-lg transition duration-300">
          <h3 className="text-lg font-semibold text-purple-700 mb-1">{item.title}</h3>
          <p className="text-sm text-gray-600 italic mb-2">{item.summary}</p>
          <p className="text-sm text-gray-800"><strong>Artificial Intelligence:</strong> {item.ai}</p>
          <p className="text-xs text-gray-500 my-1">
            <strong>ISO Standards:</strong>
            <ul className="list-disc list-inside mt-1">
              {item.iso.map((standard, idx) => (
                <li key={idx}>{standard}</li>
              ))}
            </ul>
          </p>
          <div className="mt-2 text-sm bg-purple-50 p-2 rounded text-purple-700">
            <strong>Persona:</strong> {item.persona}
          </div>
        </div>
      ))}
    </div>
  );
}
